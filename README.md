# <img src="https://crevia.xyz/Zxtni/assets/robot.png" width="24" height="24"> ZxtniSync

**A next-gen Telegram multi-account forwarder — shielded with protection, powered by adaptive rate-limits, and driven by intelligent sync to keep your channels safe, fast, and always in perfect flow.**

![Python](https://img.shields.io/badge/Python-3.7+-3776AB?style=flat&logo=python&logoColor=white)
![Telethon](https://img.shields.io/badge/Telethon-1.34+-0088CC?style=flat&logo=telegram&logoColor=white)
![License](https://img.shields.io/badge/License-AGPL--3.0-red?style=flat)
![Status](https://img.shields.io/badge/Status-Active-success?style=flat)

---

## <img src="https://crevia.xyz/Zxtni/assets/feature.png" width="24" height="24"> Features

- <img src="https://crevia.xyz/Zxtni/assets/user.png" width="24" height="24"> **Multi-Account Forwarding** - Run multiple accounts in parallel for maximum efficiency
- <img src="https://crevia.xyz/Zxtni/assets/shield.png" width="24" height="24"> **Flood-Wait Protection** - Auto wait, resume, no lost progress on rate limits
- <img src="https://crevia.xyz/Zxtni/assets/progress.png" width="24" height="24"> **Progress Tracking** - Real-time progress bars with ETA per account
- <img src="https://crevia.xyz/Zxtni/assets/speed.png" width="24" height="24"> **Adaptive Speed Modes** - Choose from `safe`, `standard`, `max`, and advanced pattern modes
- <img src="https://crevia.xyz/Zxtni/assets/log.png" width="24" height="24"> **Full Logging** - Complete activity logs saved to `zxtni_logs.txt`
- <img src="https://crevia.xyz/Zxtni/assets/range.png" width="24" height="24"> **Smart Range Splitting** - Intelligent message range distribution across accounts
- <img src="https://crevia.xyz/Zxtni/assets/save.png" width="24" height="24"> **Graceful Shutdown** - Save progress and resume from where you left off

---

## <img src="https://crevia.xyz/Zxtni/assets/install.png" width="24" height="24"> Installation

Clone this repository and run the script:

```bash
git clone https://github.com/zxtni/ZxtniSync.git
cd ZxtniSync
python3 zxtni.py
```

The script automatically installs all requirements (`Telethon`, `tqdm`, `requests`, `Pillow`) with fallbacks to system pip or a local virtual environment.  
No manual setup is needed.

---

## <img src="https://crevia.xyz/Zxtni/assets/lock.png" width="24" height="24"> Password Protection

The script uses remote password authentication:

- <img src="https://crevia.xyz/Zxtni/assets/verified.png" width="24" height="24"> **SHA256 Verification** - Password is verified against a remote hash
- <img src="https://crevia.xyz/Zxtni/assets/security.png" width="24" height="24"> **Secure Access** - Only users with the correct password can run the script
- <img src="https://crevia.xyz/Zxtni/assets/attempt.png" width="24" height="24"> **Attempt Limits** - Maximum 3 attempts to prevent brute force

---

## <img src="https://crevia.xyz/Zxtni/assets/play.png" width="24" height="24"> Usage

1. <img src="https://crevia.xyz/Zxtni/assets/account.png" width="24" height="24"> **Setup Accounts** - On first run, specify how many accounts you want to add
2. <img src="https://crevia.xyz/Zxtni/assets/api.png" width="24" height="24"> **Enter Credentials** - Provide the **API ID** and **API Hash** for each account
3. <img src="https://crevia.xyz/Zxtni/assets/source.png" width="24" height="24"> **Select Source** - Choose the source channel (applies to all accounts)
4. <img src="https://crevia.xyz/Zxtni/assets/destination.png" width="24" height="24"> **Select Destination** - Choose the destination channel (applies to all accounts)
5. <img src="https://crevia.xyz/Zxtni/assets/range.png" width="24" height="24"> **Set Range** - Enter message range (e.g., `20000-25000`) or `all` for complete forwarding
6. <img src="https://crevia.xyz/Zxtni/assets/speed.png" width="24" height="24"> **Choose Speed Mode**:
   - `safe` → maximum protection (3s delay)
   - `standard` → balanced (1s delay)
   - `max` → fastest possible
   - `pattern` → custom delay pattern
   - `bypass_random` → randomized timing (high risk)

The script runs with an ASCII banner, tagline, and live progress bars for each account.

---

## <img src="https://crevia.xyz/Zxtni/assets/folder.png" width="24" height="24"> File Structure

```
ZxtniSync/
├── zxtni.py                  # Main application script
├── README.md                  # This file
├── requirements.txt           # Auto-generated dependencies
├── zxtni_config.json         # Account configuration
├── zxtni_progress.json       # Progress tracking (resume on restart)
├── zxtni_logs.txt            # Complete activity logs
├── .zxtni_profile.png        # Temporary profile picture cache
└── *.session                 # Telegram session files (one per account)
```

---

## <img src="https://crevia.xyz/Zxtni/assets/robotic-hand.png" width="24" height="24"> Technologies Used

- **Python 3.7+** - Core programming language
- **Telethon** - Asynchronous Telegram client library
- **asyncio** - Concurrent account execution
- **tqdm** - Progress bars and ETA calculations
- **Pillow (PIL)** - Image processing for profile pictures
- **requests** - HTTP requests for remote authentication

---

## <img src="https://crevia.xyz/Zxtni/assets/jigsaw.png" width="24" height="24"> Key Features Breakdown

### <img src="https://crevia.xyz/Zxtni/assets/multi-account.png" width="24" height="24"> Multi-Account System
- Parallel account execution for maximum throughput
- Independent progress tracking per account
- Smart range splitting for balanced workload

### <img src="https://crevia.xyz/Zxtni/assets/shield.png" width="24" height="24"> Protection & Safety
- Automatic flood-wait handling with auto-resume
- Progress persistence across restarts
- Graceful error handling and recovery

### <img src="https://crevia.xyz/Zxtni/assets/modes.png" width="24" height="24"> Speed Modes
- **Safe Mode** - 3-second delays for maximum safety
- **Standard Mode** - 1-second delays for balanced speed
- **Max Mode** - No delays for maximum speed
- **Pattern Mode** - Custom delay sequences
- **Bypass Random** - Randomized timing (use with caution)

---

## <img src="https://crevia.xyz/Zxtni/assets/window.png" width="24" height="24"> System Support

- <img src="https://crevia.xyz/Zxtni/assets/linux.png" width="24" height="24"> **Linux** - Full support (Ubuntu, Debian, etc.)
- <img src="https://crevia.xyz/Zxtni/assets/windows.png" width="24" height="24"> **Windows** - Full support (Windows 10+)
- <img src="https://crevia.xyz/Zxtni/assets/android.png" width="24" height="24"> **Android Termux** - Optimized support with auto-detection
- <img src="https://crevia.xyz/Zxtni/assets/macos.png" width="24" height="24"> **macOS** - Full support with virtual environment fallback

---

## <img src="https://crevia.xyz/Zxtni/assets/license.png" width="24" height="24"> License

This project is released under **AGPL-3.0** for maximum protection.  
Any modifications deployed publicly (including SaaS) must release their source code.

---

## <img src="https://crevia.xyz/Zxtni/assets/positive-vote.png" width="24" height="24"> Acknowledgments

- **Telethon** - Powerful Telegram client library
- **tqdm** - Beautiful progress bars
- **Python Community** - Amazing ecosystem and support

---

## <img src="https://crevia.xyz/Zxtni/assets/support.png" width="24" height="24"> Support & Contact

<img src="https://crevia.xyz/Zxtni/assets/telegram.png" width="24" height="24"> **Telegram:** [@zxtni](https://telegram.me/iNToLogs)  
<img src="https://crevia.xyz/Zxtni/assets/github.png" width="24" height="24"> **GitHub:** [github.com/zxtni](https://github.com/zxtni)  
<img src="https://crevia.xyz/Zxtni/assets/website.png" width="24" height="24"> **Website:** [www.zxtni.me](https://www.zxtni.me)  
<img src="https://crevia.xyz/Zxtni/assets/partners.png" width="24" height="24"> **Organization:** [www.zxtni.dev](https://www.zxtni.dev)

---

<div align="center">

**Made with <img src="https://crevia.xyz/Zxtni/assets/hearts.png" width="24" height="24"> by Rahul - Zxtni**

**© 2025 Zxtni - All rights reserved**

![ZXTNI](https://img.shields.io/badge/🚀-ZXTNI%20PROJECTS-blue?style=for-the-badge)

</div>