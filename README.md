# go-cesu8

Package cesu8 implements functions and constants to support text encoded in [CESU-8](https://www.unicode.org/reports/tr26/tr26-4.html).
It implements functions comparable to the unicode/utf8 package for UTF-8 de- and encoding.


Extracted from https://github.com/SAP/go-hdb/blob/master/internal/unicode/cesu8.

```go
utf8Encoded := "Hello 👋"
// 48 65 6C 6C 6F 20 F0 9F 91 8B

cesu8Encoded := cesu8.EncodeString(utf8Encoded)
// 48 65 6C 6C 6F 20 ED A0 BD ED B1 8B

utf8Encoded = cesu8.DecodeString(cesu8Encoded)
// 48 65 6C 6C 6F 20 F0 9F 91 8B
```

