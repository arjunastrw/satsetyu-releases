<div align="center">

<h1>📸 satsetyu</h1>

<h3>Shoot the event. satsetyu gets every photo onto Fotoyu while you're still shooting.</h3>

<p>
A desktop uploader for Fotoyu creators: it watches your card or FTP folder, grades and<br/>
watermarks each frame, uploads in the background, retries on its own and picks up where it stopped.<br/>
This repository hosts the <b>public beta installers</b> for <b>macOS · Windows</b>.
</p>

<p>
  <a href="https://github.com/arjunastrw/satsetyu-releases/releases/latest"><img alt="Download" src="https://img.shields.io/badge/download-latest%20beta-111827?style=for-the-badge&logo=github&logoColor=white"></a>
  <img alt="macOS" src="https://img.shields.io/badge/macOS-11%2B-000000?style=for-the-badge&logo=apple&logoColor=white">
  <img alt="Windows" src="https://img.shields.io/badge/Windows-10%20%C2%B7%2011-0078D4?style=for-the-badge&logo=windows&logoColor=white">
</p>

<p>
  <img alt="Status" src="https://img.shields.io/badge/status-public%20beta-F5A623?style=flat-square">
  <img alt="Trial" src="https://img.shields.io/badge/trial-3%20days%20per%20computer-22C55E?style=flat-square">
  <img alt="Market" src="https://img.shields.io/badge/market-Indonesia-E11D48?style=flat-square">
  <img alt="License" src="https://img.shields.io/badge/license-proprietary%20beta-111827?style=flat-square">
</p>

<sub><b>Free to try, not open source.</b> The installers are licensed for evaluation only. See <a href="LICENSE">LICENSE</a>.<br/>
satsetyu is an independent tool and is not affiliated with Fotoyu.</sub>

</div>

<br/>

---

## ✦ Why satsetyu

It's 6 am at Car Free Day on Sudirman. You shoot a thousand runners in two hours. The old routine:
every 10–15 minutes walk back to the laptop, pull the card, drag files into a browser tab, wait,
and hope nothing failed while you were gone. Meanwhile the runners who want to buy their photo are
already scrolling Fotoyu.

<table>
<tr>
<td width="33%" valign="top">

### ⚡ Upload while you shoot

Point the camera's FTP at the built-in server, or drop the card into the session folder. New frames
are queued the moment they finish copying, then compressed and uploaded in parallel batches.

</td>
<td width="33%" valign="top">

### 🛟 Never lose a frame

Every photo lives in a local queue. Network drops pause the queue instead of burning retries,
half-copied files wait until they're complete, and a restart resumes exactly where it stopped.

</td>
<td width="33%" valign="top">

### 🎨 Your look, your mark

Apply a `.cube` LUT and a PNG watermark (3×3 grid, Normal / Multiply / Overlay) to every upload,
without touching the original files on your card.

</td>
</tr>
</table>

---

## ✦ The beta in one table

|                              |                                                                                                                                             |
| ---------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- |
| 🧪 **Free for 3 days**       | The trial starts the first time you open satsetyu on a computer and lasts 72 hours. A small badge in the top bar shows the time left.       |
| 🔒 **Then it locks**         | When the trial ends, uploads and the FTP server stop immediately and satsetyu shows a lock screen. Reinstalling does not restart the trial. |
| 🗂️ **Your data stays**       | Sessions, settings and the upload queue remain on your computer. Nothing is deleted when the trial ends.                                    |
| 🕰️ **Keep the clock honest** | Setting the computer clock back locks satsetyu until the clock is correct again. Turn on automatic date & time.                             |
| 🔁 **Updates**               | Open **Opsi → Cek update sekarang** to download and install a newer beta build from this repository in one click.                           |
| 📅 **Beta builds expire**    | Each beta build stops working 30 days after it was published. Download the latest build to keep testing.                                    |

---

## ✦ Download

Grab the file for your computer from the **[latest release](https://github.com/arjunastrw/satsetyu-releases/releases/latest)**:

| Your computer                            | File to download                   |
| ---------------------------------------- | ---------------------------------- |
| Mac with Apple Silicon (M1, M2, M3, M4…) | `satsetyu_<version>_aarch64.dmg`   |
| Mac with Intel processor                 | `satsetyu_<version>_x64.dmg`       |
| Windows 10 / 11 (64-bit)                 | `satsetyu_<version>_x64-setup.exe` |

<sub>Not sure which Mac you have? Apple menu → <b>About This Mac</b>: "Chip Apple M…" means Apple Silicon, "Processor Intel…" means Intel. The <code>.app.tar.gz</code>, <code>.sig</code> and <code>latest.json</code> files are for auto-update; you don't need them.</sub>

---

## ✦ Install

The beta builds are **not code-signed yet**, so macOS and Windows show a warning the first time.
That's expected for this beta; here's how to get past it.

### 🍎 macOS

1. Open the `.dmg` and drag **satsetyu** into **Applications**.
2. Open satsetyu from Applications. macOS says it can't verify the developer.
3. Go to **System Settings → Privacy & Security**, scroll down and click **Open Anyway** next to the
   satsetyu message, then confirm with your password.
4. If macOS instead says the app **"is damaged and can't be opened"**, run this once in Terminal, then
   open satsetyu again:

   ```bash
   xattr -dr com.apple.quarantine /Applications/satsetyu.app
   ```

5. When macOS asks whether satsetyu may use the **"satsetyu" keychain item**, click **Always Allow**.
   satsetyu stores your Fotoyu session there. After an update macOS may ask once more.

### 🪟 Windows

1. Run `satsetyu_<version>_x64-setup.exe`. It installs for your user only; no administrator rights needed.
2. If **"Windows protected your PC"** appears, click **More info → Run anyway**.
3. The installer downloads Microsoft Edge WebView2 automatically if your PC doesn't have it yet.
4. When you start the built-in FTP server, allow satsetyu through **Windows Defender Firewall** on
   **private networks** so your camera can reach it.

---

## ✦ First run

1. **Login Akun Fotoyu**: sign in on Fotoyu's own login page inside satsetyu. Your password never
   touches satsetyu; only the session token is kept, in your OS keychain.
2. **Info Konten**: set the price, location or FotoTree tag and description for the event.
3. **Folder Sumber Upload**: pick the folder your card or camera writes to, or turn on **FTP Kamera**.
4. Press **Mulai** on **Upload dan Monitor**. New photos are uploaded as soon as they land.

---

## ✦ Platform support

|                                    | macOS (Apple Silicon) |       macOS (Intel)        |      Windows 10 / 11       |
| ---------------------------------- | :-------------------: | :------------------------: | :------------------------: |
| Installer                          |        `.dmg`         |           `.dmg`           |       `.exe` (NSIS)        |
| Minimum version                    |       macOS 11        |          macOS 11          |     Windows 10 64-bit      |
| Verified with a real Fotoyu upload |          ✅           | ◻️ <sub>beta testing</sub> | ◻️ <sub>beta testing</sub> |
| Code signing                       |           —           |             —              |             —              |

<sub>satsetyu is developed and verified on Apple Silicon. The Intel Mac and Windows builds come from the same code and the same CI pipeline, and this beta is how they get tested in the field. Please report anything odd.</sub>

---

## ✦ Privacy

- satsetyu talks only to **Fotoyu** (login, uploads) and to **GitHub** (update checks and downloads).
- No analytics and no tracking.
- Your Fotoyu session token is stored in the macOS Keychain or Windows Credential Manager, never in a plain file.
- Photos are processed on your computer; the originals on your card are never modified.

---

## ✦ Need more time or found a bug?

- **Access after the beta**: contact details (email and WhatsApp) will be listed here soon.
- **Bug reports and feedback**: open an [issue](https://github.com/arjunastrw/satsetyu-releases/issues).
  Attach the file from **Opsi → Diagnostik**; it never contains your token or password.

---

<div align="center">
<sub>© 2026 arjunastrw · Free beta for evaluation · Proprietary, not open source · Not affiliated with Fotoyu</sub>
</div>
