# 🌐 5.1 Binary Number Systems

**Cisco Networking Academy | Solent University**

**Course:** CCNA: Introduction to Networks  
**Module:** 05 - Number Systems 
**Focus Area:** Binary Numbers, IPv4 Addressing, Positional Notation and Binary–Decimal Conversion

## 🎯 Objective

Understand how binary numbers represent IPv4 addresses, how positional notation works, and how to convert between binary and decimal numbers.

## 🧠 5.1.1 Binary and IPv4 Addresses

Computers and networking devices use the **binary number system (base 2)** to represent and process data.

Binary uses only two digits:

- **0:** Represents a binary value of zero.
- **1:** Represents a binary value of one.

Each binary digit is called a **bit**.

### IPv4 Address Structure

An **IPv4 address** is a 32-bit logical address used to identify a network interface on an IPv4 network.

- Contains **32 bits**, divided into four groups of 8 bits.
- Each group of 8 bits is called an **octet**.
- Each octet represents a decimal value between **0 and 255**.
- IPv4 addresses are commonly written in **dotted-decimal notation**.

**Example:**

`192.168.1.10`

In binary:

`11000000.10101000.00000001.00001010`

| Octet | Decimal | Binary |
|---|---|---|
| 1 | 192 | 11000000 |
| 2 | 168 | 10101000 |
| 3 | 1 | 00000001 |
| 4 | 10 | 00001010 |

> **NOTE:** Dotted-decimal notation makes IPv4 addresses easier for humans to read, while binary represents the underlying bit values used by networking devices.

## 🧠 5.1.2 Binary Positional Notation

The **decimal number system (base 10)** uses ten digits (0–9), while the **binary number system (base 2)** uses only two digits (0 and 1).

Both systems use **positional notation**, meaning each digit's value depends on its position.

### Decimal vs Binary Positional Values

| Position | Decimal (Base 10) | Binary (Base 2) |
|---|---|---|
| 8 | 10⁷ = 10,000,000 | 2⁷ = 128 |
| 7 | 10⁶ = 1,000,000 | 2⁶ = 64 |
| 6 | 10⁵ = 100,000 | 2⁵ = 32 |
| 5 | 10⁴ = 10,000 | 2⁴ = 16 |
| 4 | 10³ = 1,000 | 2³ = 8 |
| 3 | 10² = 100 | 2² = 4 |
| 2 | 10¹ = 10 | 2¹ = 2 |
| 1 | 10⁰ = 1 | 2⁰ = 1 |

> **NOTE:** In both systems, positional values increase from right to left. 
> Decimal positions are powers of 10, while binary positions are powers of 2.

### Example: Convert Binary to Decimal

An **octet** contains 8 bits. Each octet of an IPv4 address can be converted from binary to decimal using positional values.

**Example:** Convert the binary octet `11000000` to decimal.

| Bit position | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 |
|---|---|---|---|---|---|---|---|---|
| **Power of 2** | 2⁷ | 2⁶ | 2⁵ | 2⁴ | 2³ | 2² | 2¹ | 2⁰ |
| **Positional value** | 128 | 64 | 32 | 16 | 8 | 4 | 2 | 1 |
| **Binary digit** | **1** | **1** | 0 | 0 | 0 | 0 | 0 | 0 |

Add the positional values where the binary digit is **1**:

**128 + 64 = 192**

Therefore:

**11000000 (binary) = 192 (decimal)**

> **Remember:** A binary digit of **1** means include its positional value; a digit of **0** means ignore it.

## 🧠 5.1.3 Convert a Full IPv4 Address from Binary to Decimal

An IPv4 address contains **32 bits divided into four octets**. To convert it from binary to decimal, calculate the value of each octet separately.

### Example: Binary to Dotted-Decimal IPv4

**Binary IPv4 address:**

`11000000.10101000.00000001.01100101`

### Convert Each Octet

Each octet contains **8 bits**, with positional values calculated using powers of 2.

| Position | 2⁷ | 2⁶ | 2⁵ | 2⁴ | 2³ | 2² | 2¹ | 2⁰ | Decimal Calculation |
|---|---|---|---|---|---|---|---|---|---|
| **Value** | **128** | **64** | **32** | **16** | **8** | **4** | **2** | **1** | |
| **Octet 1** | 1 | 1 | 0 | 0 | 0 | 0 | 0 | 0 | 128 + 64 = **192** |
| **Octet 2** | 1 | 0 | 1 | 0 | 1 | 0 | 0 | 0 | 128 + 32 + 8 = **168** |
| **Octet 3** | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 1 | **1** |
| **Octet 4** | 0 | 1 | 1 | 0 | 0 | 1 | 0 | 1 | 64 + 32 + 4 + 1 = **101** |

### Final IPv4 Address

**Binary:** `11000000.10101000.00000001.01100101`
**Decimal:** `192.168.1.101`

> **Remember:** Add the positional values where the bits are **1**, convert each octet separately, then join the four decimal values using dots.

## 🧠 5.1.4 Decimal to Binary Conversion

To convert a decimal number into binary, use the **powers of 2** to determine which bit positions are needed to represent the number.

For IPv4 addresses, each octet contains **8 bits**, representing decimal values from **0 to 255**.

### Example: Convert Decimal 45 to Binary

**Step 1:** Start with the largest positional value (128) and work from left to right.

**Step 2:** If the remaining decimal value is greater than or equal to the positional value, write **1** and subtract it. Otherwise, write **0**.

**Step 3:** Continue until all eight bit positions are filled.

| Bit position | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 |
|---|---|---|---|---|---|---|---|---|
| **Power of 2** | 2⁷ | 2⁶ | 2⁵ | 2⁴ | 2³ | 2² | 2¹ | 2⁰ |
| **Positional value** | 128 | 64 | 32 | 16 | 8 | 4 | 2 | 1 |
| **Binary digit** | 0 | 0 | **1** | 0 | **1** | **1** | 0 | **1** |

### Calculation

- 45 is less than 128 and 64 → Write **0** for both.
- 45 − 32 = **13** → Write **1**.
- 13 is less than 16 → Write **0**.
- 13 − 8 = **5** → Write **1**.
- 5 − 4 = **1** → Write **1**.
- 1 is less than 2 → Write **0**.
- 1 − 1 = **0** → Write **1**.

**Result:** `45` (decimal) = `00101101` (binary).

> **Remember:** Start with the largest power of 2. Write **1** when you can subtract that value, otherwise write **0**. Every IPv4 octet must contain exactly 8 bits.

## 📌 Key Concepts to Remember

- **Binary (base 2)** uses two digits: 0 and 1.
- **Decimal (base 10)** uses ten digits: 0–9.
- An **IPv4 address** contains 32 bits divided into four 8-bit octets.
- Each octet represents a decimal value between **0 and 255**.
- Binary positional values are powers of 2: **128, 64, 32, 16, 8, 4, 2, 1**.
- **Binary to decimal:** Add the positional values where the bits are 1.
- **Decimal to binary:** Use positional values to determine which bits are 1 or 0.
- **Dotted-decimal notation** makes IPv4 addresses easier to read.

## 🔐 Security Relevance

Understanding binary numbers is important for network configuration and security.

- **Subnetting:** Binary calculations help determine network addresses, subnet masks and valid host ranges.
- **Access Control Lists (ACLs):** IP addresses and wildcard masks are used to permit or deny network traffic.
- **Network troubleshooting:** Understanding IP addressing helps identify incorrect configurations and connectivity problems.