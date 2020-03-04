# uid2account

This script parses the output of "check_quota.pl - nagios plugin to check Linux
filesystem quotas using repquota" to show users with their account names instead
of their guid.

## Installation

With `python3` installed, place the `uid2account` script where you like.

## Usage

Pipe the output of `check_quota.pl` to `uid2account` for a slightly improved
report:

``` shell
/usr/lib64/nagios/plugins/check_quota.pl -u all | uid2account
```

## Example

``` text
OK - All 3 users are ok.
OK - hacker          : 20.00K / 52.00G
OK - kasim           : 9.83G / 52.00G
OK - tweakit         : 31.38G / 52.00G
```
## About

This script was developed for internal use at [AMOLF][].

[AMOLF]: https://amolf.nl/
