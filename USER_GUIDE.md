# MicKeYShare — User Guide

**Your Local Files. Shared Beautifully.**

MicKeYShare lets you share any folder on your Windows PC with phones, tablets, and other computers on the same Wi-Fi or local network—no internet, no cloud upload, and no installation required.

---

## 1. Easy Download & Launch (No Installation Needed)

1. Open the official **Releases** page:
   **https://github.com/MicKeY-TM/LanFileSharing/releases/latest**
   *(Or click **Releases** on the right side of the GitHub page.)*
2. Under **Assets**, click **`MicKeYShare.exe`** to download it.
3. Save it anywhere you like (for example: **Desktop**, **Downloads**, or a **USB drive**).
4. **Double-click `MicKeYShare.exe`** to open it immediately.
   - *Note:* If Windows SmartScreen asks *"Windows protected your PC"*, click **More info** → **Run anyway** (this appears for newly downloaded unsigned standalone `.exe` files).
   - No admin rights, Python, or setup wizard are needed.

---

## 2. How to Share a Folder from Your PC

1. **Choose a Folder:**
   - Click **Browse Folder** and pick any folder or secondary drive (for example `D:\Photos` or `Documents\Projects`).
   - *Note:* The system drive root `C:\` is blocked for your safety, though subfolders inside `C:\` (like `C:\Users\YourName\Desktop`) work normally.
2. **Pick an Access Mode:**
   - **Download Only** *(Default)*: Visitors can view, preview, and download files. They cannot upload anything.
   - **Allow Uploads**: Visitors can also upload files or folders into the shared folder.
3. **Click `START SHARING`:**
   - MicKeYShare automatically finds your local Wi-Fi/LAN IP address, selects a free port, starts the local server, and displays a **QR Code** and **Sharing URL** (like `http://192.168.1.105:54321`).
   - Status at the top changes to **`● ONLINE`**.

---

## 3. Opening Files on Your Phone or Another PC

1. Make sure your phone or other device is connected to the **same Wi-Fi network** as your PC.
2. Open your phone's **Camera app** (or QR scanner) and point it at the QR code on your PC screen—or type the **LAN URL** into your browser (Chrome, Safari, Edge, Firefox).
3. Browse your files:
   - **Switch Views:** Choose **Grid**, **List**, or **Large Icons** (great for photos).
   - **Filter & Sort:** Filter by *All Files, Images, Videos, Audio, Documents, Archives* or sort by name, size, date, or type.
   - **Search:** Type in the search bar to find files and folders inside the share.
   - **Preview:** Tap images (zoom + prev/next), videos, audio, PDFs, or text/code files to preview them right in the browser.
   - **Download One or Many:**
     - Tap the download icon on any file (or folder to download it as a `.zip`).
     - Tap the checkboxes on multiple files/folders and click **Download Selected** in the bottom floating bar to download everything together as a `.zip`.
   - **Upload (if enabled by host):** Tap **Upload** (or drag and drop files on desktop) to send files back to the PC. Existing files are never silently overwritten.

---

## 4. Optional PIN Lock & Settings

Click **Settings** in the top-right corner of the desktop app to customize:
- **Light / Dark Theme** and **Default Web View**
- **Require PIN to Access:** Set a 4+ character PIN so visitors must unlock before browsing.
- **Max Upload Size (MB):** Limit maximum upload size (or set *Unlimited*).
- **Network Interface / Port:** Leave on *Auto* unless you use multiple adapters (e.g. VPN + Wi-Fi).
- **Show Hidden Files:** Toggle whether hidden/dot files appear.
- **Portable Config Mode:** Saves your preferences in `mickeyshare.config.json` right next to `MicKeYShare.exe`.

---

## 5. Stopping Access Immediately

When you are done sharing:
- Click **`STOP SHARING`** (or simply close the MicKeYShare window).
- The server stops immediately, releases the port, and **all connected phones/browsers lose access right away**.

---

## 6. Troubleshooting

- **Phone cannot open the URL:**
  1. Confirm both devices are on the **same Wi-Fi network** (not Guest Wi-Fi with AP isolation, and not mobile data).
  2. Click **Firewall Help** on the sharing screen to allow inbound LAN access in Windows Defender Firewall, or ensure your Windows Wi-Fi network profile is set to **Private** (Settings → Network & internet → Wi-Fi → Private network).
  3. If you have a VPN active, either pause it or pick your Wi-Fi IP inside **Settings → Network Interface**.
- **Where are logs saved?**
  - Local diagnostic logs are written to `logs/mickeyshare.log` (never sent anywhere).
