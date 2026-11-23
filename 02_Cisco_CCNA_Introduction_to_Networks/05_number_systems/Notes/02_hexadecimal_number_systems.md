# 🌐 5.2 Hexadecimal Number System

**Cisco Networking Academy | Solent University**

**Course:** CCNA: Introduction to Networks  
**Module:** 05 - Number Systems   
**Focus Area:** Hexadecimal Numbers, IPv6 Addressing, Decimal-to-Hexadecimal Conversion and Hexadecimal-to-Decimal Conversion  

## 🎯 Objective

Understand how the hexadecimal number system represents values using base 16, recognise its use in IPv6 addresses, and learn how to convert between decimal and hexadecimal numbers.

## 🧠 5.2.1 Decimal to Hexadecimal Conversion

The **hexadecimal number system (base 16)** uses 16 symbols to represent numerical values.

- **0–9:** Represent decimal values 0 to 9.
- **A–F:** Represent decimal values 10 to 15.

### Hexadecimal Values

| Decimal | Hexadecimal | Binary |
|---|---|---|
| 0 | 0 | 0000 |
| 1 | 1 | 0001 |
| 2 | 2 | 0010 |
| 3 | 3 | 0011 |
| 4 | 4 | 0100 |
| 5 | 5 | 0101 |
| 6 | 6 | 0110 |
| 7 | 7 | 0111 |
| 8 | 8 | 1000 |
| 9 | 9 | 1001 |
| 10 | A | 1010 |
| 11 | B | 1011 |
| 12 | C | 1100 |
| 13 | D | 1101 |
| 14 | E | 1110 |
| 15 | F | 1111 |

> **NOTE:** Each hexadecimal digit represents exactly **4 binary bits**.

### Example: Convert Decimal 45 to Hexadecimal

**Method 1:**

**Step 1:** To convert a decimal number into hexadecimal, first divide the number by **16**.
- 45 / 16 = 2.8125

**Step 2:** Take the reminder and multiply by 16. 
- 0.8125 * 16 = 13
- In hexadecimal, decimal 13 = D.

**Result:** `45` (decimal) = `2D` (hexadecimal).

Verification (Using hexadecimal positional values):  **(2 × 16) + 13 = 45**

> **Remember:** Divide by 16, record each remainder, and read the remainders from bottom to top. Hexadecimal uses **A–F** for values **10–15**.

**Method 2: Decimal → Binary → Hexadecimal**

**Step 1:** Convert decimal `45` into an 8-bit binary number using powers of 2.

| Bit position | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 |
|---|---|---|---|---|---|---|---|---|
| **Power of 2** | 2⁷ | 2⁶ | 2⁵ | 2⁴ | 2³ | 2² | 2¹ | 2⁰ |
| **Positional value** | 128 | 64 | 32 | 16 | 8 | 4 | 2 | 1 |
| **Binary digit** | 0 | 0 | **1** | 0 | **1** | **1** | 0 | **1** |

**Calculation:** 32 + 8 + 4 + 1 = **45**
**Binary:** `00101101`

**Step 2:** Divide the binary number into two groups of four bits, starting from the right.

`0010` and `1101`

**Step 3:** Convert each group of four bits into its hexadecimal equivalent.

| Binary Group | Decimal Calculation | Decimal | Hexadecimal |
|---|---|---|---|
| `0010` | 2 | 2 | **2** |
| `1101` | 8 + 4 + 1 | 13 | **D** |

**Result:** `45` (decimal) = `2D` (hexadecimal).

> **Remember:** Convert decimal to binary, group the bits into sets of four from right to left, then replace each group with its hexadecimal digit.

## 🧠 5.2.2 Hexadecimal to Decimal Conversion

To convert a hexadecimal number into decimal, multiply each hexadecimal digit by its **positional value (power of 16)**, then add the results together.

Hexadecimal uses **base 16**, meaning each position represents a power of 16, increasing from right to left.

### Hexadecimal Positional Values

| Position | 4 | 3 | 2 | 1 |
|---|---|---|---|---|
| **Power of 16** | 16³ | 16² | 16¹ | 16⁰ |
| **Positional value** | 4096 | 256 | 16 | 1 |

> **NOTE:** Hexadecimal digits **A–F** represent decimal values **10–15**.


### Example: Convert Hexadecimal 2D to Decimal

**Method 1:**

**Step 1:** Identify the decimal value of each hexadecimal digit.

- `2` = 2
- `D` = 13

**Step 2:** Multiply each digit by its positional value.

| Position | 2 | 1 |
|---|---|---|
| **Power of 16** | 16¹ | 16⁰ |
| **Positional value** | 16 | 1 |
| **Hexadecimal digit** | 2 | 13 (D) |
| **Calculation** | 2 × 16 = **32** | 13 × 1 = **13** |

**Step 3:** Add the results together.
32 + 13 = 45

**Result:** `2D` (hexadecimal) = `45` (decimal).

> **Remember:** Multiply each hexadecimal digit by its corresponding power of 16, then add the results. Convert **A–F** into decimal values **10–15** before calculating.

**Method 2: Hexadecimal → Binary → Decimal**

**Step 1:** Convert each hexadecimal digit into its 4-bit binary equivalent.

| Hexadecimal | Decimal | Binary |
|---|---|---|
| 2 | 2 | `0010` |
| D | 13 | `1101` |

**Step 2:** Combine the two 4-bit groups into an 8-bit binary number.

`0010 1101` → `00101101`

**Step 3:** Convert the binary number into decimal using powers of 2.

| Bit position | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 |
|---|---|---|---|---|---|---|---|---|
| **Power of 2** | 2⁷ | 2⁶ | 2⁵ | 2⁴ | 2³ | 2² | 2¹ | 2⁰ |
| **Positional value** | 128 | 64 | 32 | 16 | 8 | 4 | 2 | 1 |
| **Binary digit** | 0 | 0 | **1** | 0 | **1** | **1** | 0 | **1** |

### Calculation

- 2⁵ = **32**
- 2³ = **8**
- 2² = **4**
- 2⁰ = **1**

**32 + 8 + 4 + 1 = 45**

**Result:** `2D` (hexadecimal) = `45` (decimal).

> **Remember:** Convert each hexadecimal digit into 4 bits, combine the groups, then add the positional values where the binary bits are **1**.

## 🧠 5.2.3 Hexadecimal and IPv6 Addresses

**IPv6 (Internet Protocol version 6)** uses hexadecimal notation to represent 128-bit IP addresses.

Unlike IPv4, which uses dotted-decimal notation, IPv6 uses **eight groups of four hexadecimal digits**, separated by colons (`:`).

### IPv6 Address Structure

- Contains **128 bits**, divided into eight groups of 16 bits.
- Each 16-bit group is called a **hextet**.
- Each hexadecimal digit represents **4 binary bits**.
- Each hextet contains up to **4 hexadecimal digits**.
- IPv6 addresses use **colons (`:`)** to separate hextets.

**Example:** `2001:0DB8:0000:0000:0000:FF00:0042:8329`

| Hextet | Hexadecimal | Number of Bits |
|---|---|---|
| 1 | `2001` | 16 |
| 2 | `0DB8` | 16 |
| 3 | `0000` | 16 |
| 4 | `0000` | 16 |
| 5 | `0000` | 16 |
| 6 | `FF00` | 16 |
| 7 | `0042` | 16 |
| 8 | `8329` | 16 |

**Total:** 8 × 16 = **128 bits**

> **NOTE:** Hexadecimal makes long IPv6 addresses easier to read and write than their full binary representation.

### IPv6 Address Compression

IPv6 addresses can be shortened using two rules:

Full IPv6 address: `2001:0DB8:0000:0000:0000:FF00:0042:8329`

- **Leading zeros:** Remove leading zeros within each hextet.
Result: `2001:**DB8**:**0**:**0**:**0**:FF00:**42**:8329`

- **Double colon (`::`):** Replace one consecutive sequence of all-zero hextets with `::`.
**Compressed IPv6 address:** `2001:DB8::FF00:42:8329`

> **Remember:** The double colon (`::`) replaces one or more consecutive all-zero hextets. It can appear **only once** in an IPv6 address to avoid ambiguity. When multiple sequences exist, compress the longest one.

### IPv4 vs IPv6 Address Representation

| Feature | IPv4 | IPv6 |
|---|---|---|
| Address length | 32 bits | 128 bits |
| Number system | Decimal notation | Hexadecimal notation |
| Structure | 4 octets | 8 hextets |
| Separator | Dot (`.`) | Colon (`:`) |
| Example | `192.168.1.10` | `2001:DB8::1` |

## 📌 Key Concepts to Remember

- **Hexadecimal (base 16)** uses 16 symbols: **0–9 and A–F**.
- Hexadecimal letters **A–F** represent decimal values **10–15**.
- Each hexadecimal digit represents **4 binary bits**.
- **Decimal to hexadecimal:** Divide by 16 and use the remainders, or convert through binary.
- **Hexadecimal to decimal:** Multiply each digit by its corresponding power of 16 and add the results, or convert through binary.
- **IPv6 addresses** contain 128 bits, represented using eight 16-bit hextets.
- **IPv6 compression** removes leading zeros and uses `::` for consecutive all-zero hextets.

## 🔐 Security Relevance

Understanding hexadecimal numbers is important for IPv6 networking and security.

- **IPv6 Addressing:** Recognising hexadecimal notation helps configure and troubleshoot IPv6 addresses.
- **Access Control Lists (ACLs):** IPv6 addresses and prefixes can be used to permit or deny network traffic.
- **Network Monitoring:** Understanding IPv6 addresses helps identify devices and analyse traffic in network logs.
- **Security Troubleshooting:** Recognising IPv6 address formats helps detect incorrect configurations and investigate connectivity issues.

