# Hacking Utilities

Quick and dirty python scripts used for CTFs/hacking.

I may or may not come back to this and clean it up.

## Scripts

### ascii-vals.py

Used to convert input to its equivalent ASCII-encoding.
This is useful for evading XSS filters that escape quotation marks

### Example usage

Input. `payload` contains the string `alert(1);`

```bash
cat payload | python ascii-vals.py --javascript-payload
```

Output:

<script>eval(String.fromCharCode(97, 108, 101, 114, 116, 40, 49, 41, 59))</script>
