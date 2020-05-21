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

| charset | chars |  1  |   8  |  10  |  12  |   16  |   20  |   32  |
| ------- | ----: | --: | ---: | ---: | ---: | ----: | ----: | ----: |
| `[ -~]` |    95 | 6.6 | 52.6 | 65.7 | 78.8 | 105.1 | 131.4 | 210.2 |
