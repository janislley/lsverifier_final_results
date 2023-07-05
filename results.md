# LSVerifier analysis

Dataset analysis performed by LSVerifier tool.

## Verification results

| Software  | Version | Files Verified | Functions Verified | Counterexamples | Overall time | Peak Memory Usage |
|-----------|------------|-----------|--------------|-----------|-------------|---------------|
| VLC       | 3.0.18     | 1171      | 13709        | 72        | 1033.79s    | 20.09 MB      |
| VIM       | 9.0.1672   | 188       | 9611         | 110       | 554.56s     | 39.83MB       | 
| TMUX      | 3.3a       | 179       | 2168         | 1788      | 52218.45s   | 43.12MB       |
| RUFUS     | 4.1        | 144       | 1615         | 576       | 283.95s     | 6.06MB        |
| OpenSSH   | 9.3        | 290       | 3183         | 338       | 873.27s     | 42.58MB       |
| Cmake     | 3.27.0-rc4 | 1516      | 11279        | 552       | 934.21s     | 37.07MB       |
| Netdata   |            |           |              |           |             |               |
| Wireshark |            |           |              |           |             |               |
| OpenSSL   | 3.1.1      | 1575      | 17168        | 3140      | 6046.63s    | 53.34MB       |
| Putty     | 0.78       | 403       | 5310         | 2472      | 66210.32s   | 58.54MB       |   

## Propertie violated

| Violations | IP   | ABV   | ALB   | AUB   | SOV   | IPF   | IDO   | NP    | DZ    | AOOB  | AF    |
|-----------|-------|-------|-------|-------|-------|-------|-------|-------|-------|-------|-------|
| VLC       | 57    | 2     | 0     | 0     | 0     | 2     | 0     | 1     | 0     | 0     | 10    |
| VIM       | 100   | 3     | 1     | 2     | 0     | 2     | 0     | 2     | 0     | 0     | 0     |
| TMUX      | 1725  | 0     | 12    | 9     | 0     | 21    | 0     | 20    | 0     | 0     | 1     |
| RUFUS     | 513   | 0     | 0     | 4     | 4     | 6     | 0     | 20    | 29    | 0     | 0     |
| OpenSSH   | 311   | 3     | 4     | 0     | 0     | 4     | 1     | 10    | 5     | 0     | 0     |
| Cmake     | 481   | 28    | 5     | 2     | 18    | 7     | 0     | 6     | 2     | 0     | 3     |
| Netdata   |       |       |       |       |       |       |       |       |       |       |       |
| Wireshark |       |       |       |       |       |       |       |       |       |       |       |
| OpenSSL   | 2753  | 77    | 98    | 22    | 10    | 7     | 2     | 131   | 11    | 0     | 29    |
| Putty     | 1996  | 8     | 25    | 26    | 4     | 6     | 0     | 56    | 14    | 0     | 337   |

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
* AOOB: Access to Object Out of Bounds
* AF: Assertion Failure
