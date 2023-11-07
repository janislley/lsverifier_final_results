# LSVerifier analysis

Dataset analysis performed by LSVerifier tool.

report. This approach can systematically guide a bounded model checker to verify large open-source software systems.

## Short introduction

Computer-based systems have solved several domain problems, including industrial, military, education, and wearable. Nevertheless, such arrangements need high-quality software to guarantee security and safety as both are mandatory for modern software products. We advocate that bounded model-checking techniques can efficiently detect vulnerabilities in general software systems. However, such an approach struggles to scale up and verify extensive code bases. Consequently, we have developed and evaluated a methodology to verify large software systems using a state-of-the-art bounded model checker. In particular, we pre-process input source-code files and guide the respective model checker to explore them systematically. Moreover, the proposed scheme includes a function-wise prioritization strategy, which readily provides results for code entities according to a scale of importance. Experimental results using a real implementation of the proposed methodology show that it can efficiently verify large software systems. Besides, it presented low peak memory allocation when executed. We have evaluated our approach by verifying twelve popular open-source C projects, where we have found real software vulnerabilities that their developers confirmed.

## Command to verify

~~~
lsverifier -v -r -f -l dep.txt
~~~

## Verification results

| Software  | Version      | Property Violations | Files Verified | External Includes | Code lines | Functions Verified | Overall time | Peak Memory Usage |
|-----------|--------------|---------------------|----------------|-------------------|------------|--------------------|--------------|-------------------|
| VLC       | 3.0.18       | 72                  | 1171           | 289               | 421840     | 13709              | 1033.79s     | 20.09MB           |
| VIM       | 9.0.1672     | 110                 | 188            | 95                | 366775     | 9611               | 554.56s      | 39.83MB           |
| TMUX      | 3.3a         | 1788                | 179            | 445               | 61004      | 2168               | 52218.45s    | 43.12MB           |
| RUFUS     | 4.1          | 576                 | 144            | 108               | 56278      | 1615               | 283.95s      | 6.06MB            |
| OpenSSH   | 9.3          | 338                 | 290            | 63                | 109791     | 3183               | 873.27s      | 42.58MB           |
| Cmake     | 3.27.0-rc4   | 552                 | 1516           | 1030              | 324760     | 11279              | 934.21s      | 37.07MB           |
| Netdata   | 1.40.1       | 1318                | 307            | 160               | 312530     | 7352               | 51471.27s    | 129.09MB          |
| Wireshark | 4.0.6        | 2141                | 2330           | 77                | 4177163    | 121567             | 59952.39s    | 391.44MB          |
| OpenSSL   | 3.1.1        | 3140                | 1575           | 616               | 491632     | 17168              | 6046.63s     | 53.34MB           |
| PuTTY     | 0.78         | 2472                | 403            | 153               | 127282     | 5310               | 66210.32s    | 58.54MB           |
| SQLite    | 3.42.0       | 3265                | 340            | 609               | 258382     | 8911               | 2493.75s     | 33.22MB           |
| Redis     | 7.0.11       | 187                 | 418            | 556               | 170673     | 8211               | 727.76s      | 46.57MB           |
  

## Properties violated

| Software  | IP    | ABV   | ALB   | AUB   | SOV   | IPF   | IDO   | NP    | DZ    | AF    | AOOB  |
|-----------|-------|-------|-------|-------|-------|-------|-------|-------|-------|-------|-------|
| VLC       | 57    | 2     | 0     | 0     | 0     | 2     | 0     | 1     | 0     | 10    | 0     |
| VIM       | 100   | 3     | 1     | 2     | 0     | 2     | 0     | 2     | 0     | 0     | 0     |
| TMUX      | 1725  | 0     | 12    | 9     | 0     | 21    | 0     | 20    | 0     | 1     | 0     |
| RUFUS     | 513   | 0     | 0     | 4     | 4     | 6     | 0     | 20    | 29    | 0     | 0     |
| OpenSSH   | 311   | 3     | 4     | 0     | 0     | 4     | 1     | 10    | 5     | 0     | 0     |
| Cmake     | 481   | 28    | 5     | 2     | 18    | 7     | 0     | 6     | 2     | 3     | 0     |
| Netdata   | 1045  | 1     | 12    | 5     | 3     | 5     | 0     | 212   | 35    | 0     | 0     |
| Wireshark | 1940  | 20    | 12    | 17    | 35    | 2     | 0     | 77    | 5     | 27    | 6     |
| OpenSSL   | 2753  | 77    | 98    | 22    | 10    | 7     | 2     | 131   | 11    | 29    | 0     |
| Putty     | 1996  | 8     | 25    | 26    | 4     | 6     | 0     | 56    | 14    | 337   | 0     |
| SQLite    | 2254  | 36    | 15    | 37    | 16    | 9     | 0     | 540   | 29    | 326   | 3     |
| Redis     | 150   | 3     | 9     | 3     | 11    | 3     | 0     | 7     | 0     | 0     | 1     |

Item description:

* IP: Invalid Pointer
* ABV: Array Bounds Violated
* ALB: Array Lower Bound
* AUB: Array Upper Bound
* SOV: Same Object Violation
* IPF: Invalid Pointer Freed
* IDO: Invalidated Dynamic Object
* NP: NULL Pointer
* DZ: Division by Zero
* AF: Assertion Failure
* AOOB: Access to Object Out of Bounds


## References

* VLC: https://github.com/videolan/vlc
* VIM: https://github.com/vim/vim
* TMUX: https://github.com/tmux/tmux
* RUFUS: https://github.com/pbatard/rufus
* OpenSSH: https://github.com/openssh/openssh-portable
* Cmake: https://github.com/Kitware/CMake
* Netdata: https://github.com/netdata/netdata
* Wireshark: https://github.com/wireshark/wireshark
* OpenSSL: https://github.com/openssl/openssl
* Putty: https://github.com/github/putty
* SQLite: https://github.com/sqlite/sqlite
* Redis: https://github.com/redis/

