#  Custom Hashing (SHA-256 Comparison)

##  Name: KANISHKA S

##  Objective

Build a **custom hash function** that:
- Returns a **fixed 32-character hash**
- Can be compared side-by-side with **SHA-256** output (first 32 characters)

This project demonstrates hashing fundamentals through a simplified educational hash method and highlights the contrast with the **cryptographically secure** SHA-256.

---

##  Algorithm Logic – Custom Hash Function

The custom hashing logic is designed to be **lightweight** and **easy to understand**, focusing on how hashes can be generated:

###  Steps:
1. **Convert input characters to ASCII values**
2. **Multiply each ASCII value by its index + 1** (to introduce positional weight)
3. **Apply modulo operations** to mix values (e.g., modulo 256)
4. **Compress & pad results** into a final **32-character hexadecimal** string


---

##  Sample Output Table

| Input                       | Custom Hash                        | SHA-256 (first 32 chars)             |
|----------------------------|-------------------------------------|--------------------------------------|
| `test`                     | `1308364c000000000000000000000000` | `9f86d081884c7d659a2feaa0c55ad015`   |
| `TEST`                     | `5429372d000000000000000000000000` | `94ee059335e587e501cc4bf90613e081`   |
| `Test12345`                | `5408364c3309421c5900000000000000` | `106ac304ae39bc4029db0faf0d1734bd`   |
| `TeSt0987!@#`              | `5408374c2e330434063a5e0000000000` | `2f832ee3aa624a85ed85a7c068c61185`   |
| `longer input string for testing` | `0b1c271814051e4014351a221c3a5b4e` | `62921d9f46268b5bdc49a3c2d5193622`   |

---

##  Comparison Summary

| Criteria                     | Custom Hash                  | SHA-256                      |
|-----------------------------|------------------------------|------------------------------|
| Same input → same hash      | ✅ Yes                        | ✅ Yes                        |
| Small input change → big change | ✅ Yes                    | ✅ Yes                        |
| Cryptographically secure    | ❌ No (educational only)      | ✅ Yes                        |
| Output length               | 32-character hex             | 64-character hex (standard)  |
| Speed & Simplicity
