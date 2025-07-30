# Custom-Hashing-SHA-256
Name: KANISHKA S

Ojective
A custom hash function that returns a fixed 32-character hash, and compare it with SHA-256.

Algorithm Logic
Uses ASCII conversion

Multiplies by index + 1

Applies modulo for mixing

Compresses into 32-character hex output

Sample Output Table

Input                                   Custom Hash                             SHA-256 (first 32 chars)
--------------------------------------------------------------------------------------------------------------
test                                    1308364c000000000000000000000000        9f86d081884c7d659a2feaa0c55ad015
TEST                                    5429372d000000000000000000000000        94ee059335e587e501cc4bf90613e081
Test12345                               5408364c3309421c5900000000000000        106ac304ae39bc4029db0faf0d1734bd
TeSt0987!@#                             5408374c2e330434063a5e0000000000        2f832ee3aa624a85ed85a7c068c61185
longer input string for testing         0b1c271814051e4014351a221c3a5b4e        62921d9f46268b5bdc49a3c2d5193622


Comparison
Same input → Same hash ✔️

Small change → Very different hash ✔️

SHA-256 is cryptographically stronger

Custom hash is simpler, educational
