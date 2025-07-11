# STM32-Internal-flash-read-and-write
Read and write from/to Internal flash of STM32

# STM32F303RE Flash Memory Read/Write Example

This project demonstrates how to **read from and write to internal Flash memory** of the STM32F303RE microcontroller using STM32CubeIDE and HAL libraries.

---

## ✅ MCU: STM32F303RE

- **Flash Size**: 512 KB
- **Flash Page Size**: 2 KB (2048 bytes)
- **Flash Base Address**: `0x08000000`

---
## 📌 Configuration

- **User Data Flash Address**: `0x0807F800`
  - This is the last page of Flash (Page 255 for 512 KB)
  - You can reserve one or more pages for storing non-volatile data.

---

## 🔐 Flash Access Rules

- You **must erase a page** before writing to it.
- Writing is done in **16-bit (half-word)** units.
- Always **unlock Flash** before writing/erasing and **lock** afterward.

---

## 📦 How It Works

1. Erases the last Flash page.
2. Writes a 32-bit value (in two half-word operations).
3. Reads it back.
4. Verifies it matches the expected value.

---



