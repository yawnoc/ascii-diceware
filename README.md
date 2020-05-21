# ASCII Diceware

[Character list for ASCII Diceware.](ascii-diceware.txt)

Three dice are required.
If a toss returns `346` or higher, or corresponds to a character
which is not allowed by a [dumb password rule][dumb], then toss again.

[dumb]: https://github.com/dumb-password-rules/dumb-password-rules

## Entropy

From `U+0020 SPACE` to `U+007E TILDE` there are 95 characters,
giving `log(95) / log(2) == 6.57` bits per character.
Excluding characters will reduce the bittage.

### Total entropy for passwords of given charset and length

| charset         | chars |   1  |   8  |  10  |  12  |   16  |   20  |   32  |
| --------------- | ----: | ---: | ---: | ---: | ---: | ----: | ----: | ----: |
| `[ -~]`         |    95 | 6.57 | 52.6 | 65.7 | 78.8 | 105.1 | 131.4 | 210.2 |
| `[0-9A-Za-z+/]` |    64 | 6.00 | 48.0 | 60.0 | 72.0 |  96.0 | 120.0 | 192.0 |
| `[0-9A-Za-z]`   |    62 | 5.95 | 47.6 | 59.5 | 71.5 |  95.3 | 119.1 | 190.5 |
| `[0-9a-z]`      |    36 | 5.17 | 41.4 | 51.7 | 62.0 |  82.7 | 103.4 | 165.4 |
