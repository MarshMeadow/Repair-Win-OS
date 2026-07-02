# 🛠️ Repair-Win-OS

A collection of built-in Windows tools and command-line methods to help diagnose and repair common system issues on **Windows 10 / Windows 11**.

> ⚠️ Disclaimer:
> These tools modify system files and settings. Use at your own risk. Always ensure you understand a command before running it. This is not affiliated with Microsoft.

---

## 🧰 1. System File Checker (SFC)

Repairs missing or corrupted system files.

### ✅ Steps:

1. Open **Start Menu**
2. Search **Command Prompt**
3. Right-click → **Run as Administrator**
4. Run:

```cmd
sfc /scannow
```

### 🔎 What it does:

* Scans all protected system files
* Replaces corrupted or missing files automatically

---

## 🧰 2. DISM (Deployment Image Servicing and Management)

Fixes Windows image corruption that SFC can’t always repair.

### 🔍 Check health:

```cmd
DISM /Online /Cleanup-Image /CheckHealth
```

### 🧪 Scan for corruption:

```cmd
DISM /Online /Cleanup-Image /ScanHealth
```

### 🛠️ Repair Windows image:

```cmd
DISM /Online /Cleanup-Image /RestoreHealth
```

---

### 📦 Optional: Using a repair source (advanced)

If Windows Update cannot fix the image:

```cmd
DISM /Online /Cleanup-Image /RestoreHealth /Source:X:\Sources\install.wim /LimitAccess
```

> Replace `X:` with your mounted Windows installation media drive.

---

## 🔄 3. Reset Windows (Command Line)

Reinstalls Windows while allowing you to keep or remove files.

### Run:

```cmd
systemreset -cleanpc
```

### Or via Recovery Mode:

* Boot into **Advanced Startup**
* Go to:
  **Troubleshoot → Reset this PC**

---

## 🔁 4. System Restore (Command Prompt Method)

Restores your PC to a previous working state.

### Steps:

1. Boot into Windows or Safe Mode
2. Open **Command Prompt (Admin)**
3. Run:

```cmd
rstrui.exe
```

### 💡 Tip:

* Works best if restore points were previously enabled

---

## 🧪 5. Third-Party Repair Tools (Optional)

Some tools like system repair utilities can help automate fixes.

> ⚠️ Warning: Only download tools from trusted sources and official websites.

For more reference:
[Windows Repair Guide (reference source)](https://www.ubackup.com/windows-10/repair-windows-10-using-command-prompt.html?utm_source=chatgpt.com)

---

## 📌 Notes

* Always run Command Prompt as **Administrator**
* SFC should usually be run **before DISM**
* Restart your PC after repairs
* If problems persist, consider a clean Windows reinstall

---

## 🧠 Recommended Repair Order

1. `sfc /scannow`
2. `DISM /RestoreHealth`
3. Restart
4. System Restore (if needed)
5. Reset PC (last resort)

---

## ⚡ Extra Tip

If Windows won’t boot:

* Use **Windows Recovery Environment (WinRE)**
* Or boot from a Windows installation USB

---
