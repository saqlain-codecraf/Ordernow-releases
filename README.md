# OrderNow POS — Downloads

OrderNow POS is a restaurant point-of-sale for Windows. It works **offline** on your restaurant's own network: no internet or cloud account is needed to take orders, print kitchen tickets, take payments or close the day.

## ⬇️ Download

**[Download the latest version](https://github.com/saqlain-codecraf/Ordernow-releases/releases/latest)**

On the release page, under **Assets**, download **`OrderNow-POS-Setup-x.y.z.exe`**. You only need this one file; the others (`latest.yml`, `.blockmap`) are used by automatic updates.

## 💻 System requirements

| | Minimum |
|---|---|
| Windows | Windows 10 or 11, 64-bit |
| Memory | 4 GB RAM |
| Disk | 500 MB free (more for years of orders and backups) |
| Screen | 1280 × 720 or larger; touch screens supported |
| Network | A local network (Wi-Fi or cable) if you use more than one PC, a kitchen display or waiter phones |
| Printers | ESC/POS thermal printers (58 mm or 80 mm), network or USB — optional |

## 🛠️ Install

1. Run **`OrderNow-POS-Setup-x.y.z.exe`**.
2. Windows may show **"Windows protected your PC"** because the installer is not code-signed. Click **More info → Run anyway**.
3. Choose the install folder (or keep the default) and finish the setup. OrderNow appears in the Start menu.

## 🚀 First start (main PC)

1. Enter your **restaurant name** and **base currency**. The base currency cannot be changed after the first order.
2. Sign in with the admin PIN **`1234`**. You are asked to choose a new PIN straight away.
3. From the sidebar, set up:
   - **Menu** — categories, items, prices, sizes and extras
   - **Tables** — areas and tables
   - **Printers** — the receipt printer and one printer per kitchen or bar
   - **Users** — staff, their PINs and roles
   - **Settings** — tax, service charge, receipt text, colours

   Tip: on the **Printers** screen, **Detect printers** finds printers on the network and on this PC and fills in their details.

## 🖥️ More tills, kitchen screens and waiter phones

One PC is the **main PC**: it keeps all the data. Other devices connect to it over your network.

| Device | How to connect |
|---|---|
| **Another till PC** | Install OrderNow on it. On the first screen choose **Connect to the main PC** and enter the main PC's address and hub key. |
| **Kitchen display** | Open the kitchen link in any browser (TV, tablet, PC) and enter the hub key once. |
| **Waiter phone** | Scan the QR code or open the waiter link, enter the hub key once, and add it to the home screen. |

The addresses, QR codes and hub key are on the main PC in **Settings → Network** (turn on the hub server there). All devices must be on the same network as the main PC.

## 🔄 Updates

- OrderNow checks for a new version in the background when it starts and every few hours, and downloads it quietly.
- When it is ready, a green **Update ready** button appears in the top bar. Click it when convenient — OrderNow closes, updates and opens again in under a minute.
- It **never restarts by itself** during service. If you don't click it, the update installs the next time OrderNow is closed.
- You can also check in **Settings → Updates → Check now**.
- Each PC updates itself and needs internet only for the download. Update the main PC and the tills to the same version.

## 💾 Your data and backups

All data stays on the main PC, in `%APPDATA%\OrderNow POS\`:

| Folder | What is in it |
|---|---|
| `data` | The database: orders, menu, staff, settings |
| `backups` | Automatic daily backups (newest 30 kept) and manual backups |
| `images` | Menu pictures |
| `logs` | Logs for troubleshooting |

- **Updating or uninstalling OrderNow does not delete this folder.**
- When the PC is online, OrderNow tells the developer it is installed — restaurant name, phone, address and app version — once after setup and then once a month. Orders, sales and customer details are never sent.
- Make extra backups from **Settings → Backups**, and copy the `backups` folder to a USB drive or cloud storage now and then.
- To move to a new PC, install OrderNow there and restore a backup from **Settings → Backups**.

## ❓ Troubleshooting

| Problem | What to do |
|---|---|
| "Windows protected your PC" | Click **More info → Run anyway**. |
| A till or phone cannot connect | Check both are on the same network, the hub server is on in Settings → Network on the main PC, and Windows Firewall allows OrderNow (allow it when Windows asks). |
| Nothing prints | Check the printer is on and the address in **Printers** is right, then use **Test print**. Failed jobs wait in the print queue and can be retried. |
| Forgot the admin PIN | Another user with the *Manage users* permission can set a new PIN under **Users**. |

## 📋 Versions

| Version | Date | Notes |
|---|---|---|
| [0.3.1](https://github.com/saqlain-codecraf/Ordernow-releases/releases/tag/v0.3.1) | 28 Oct 2026 | Connects to the updated licence service |
| [0.3.0](https://github.com/saqlain-codecraf/Ordernow-releases/releases/tag/v0.3.0) | 28 Oct 2026 | Licence status: the provider can show a message or lock a POS (7 days' notice first). Contact 0349 3437606 |
| [0.2.1](https://github.com/saqlain-codecraf/Ordernow-releases/releases/tag/v0.2.1) | 28 Oct 2026 | Sends the developer a short install report (restaurant name, phone, version) once after setup and once a month |
| [0.2.0](https://github.com/saqlain-codecraf/Ordernow-releases/releases/tag/v0.2.0) | 24 Oct 2026 | Expenses, Balance sheet, customer credit accounts (pay later, receive payment, statements), Detect printers |
| [0.1.0](https://github.com/saqlain-codecraf/Ordernow-releases/releases/tag/v0.1.0) | 24 Oct 2026 | First release |

---

© OrderNow POS. All rights reserved. This repository contains installers only.
