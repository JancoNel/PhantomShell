# PhantomShield (IN DEVELOPMENT)

**PhantomShield** is an advanced, automated Blue Team defense suite designed for live CTF battlegrounds and competitive cybersecurity challenges. It hardens Windows-based targets at runtime by eliminating vulnerable services, spoofing attacker scans, and enforcing near-paranoid-level process control — all while maintaining control for the defending team through a trusted shell.

> ⚠️ Built for speed. Built for deception. Built for cyber-war.

---

## 🔰 Key Components

### `ServiceDisabler`
- Scans for predictable, exploitable Windows services.
- Terminates and disables them within seconds of deployment.
- Harden first — before the first Nmap ping finishes.

### `ServiceSpoofer`
- Spins up fake services (e.g., SSH, RDP) with spoofed banners.
- Reports vulnerable versions on scan.
- Refuses all credentials and spawns no actual shell.
- Wastes attacker time debugging exploits that never worked.

### `FirewallBouncer`
- Monitors incoming SYN packets and behavior flags.
- Uses remote MongoDB to sync attacker IPs across all blue team machines.
- Once flagged on one machine, attacker is blacklisted everywhere.
- Instantly applies Windows firewall rules on detection.

### `ProcessSniper`
- Kills known post-exploitation tools on sight.
- Targets include: `cmd.exe`, `powershell.exe`, `python.exe`, `node.exe`, etc.
- 1-second loop ensures no shell survives long enough to be useful.

### `BlueShell`
- Trusted C++ interface shell for defenders only.
- Allows controlled commands, service toggles, and logging.
- Cannot be exploited or hijacked by standard shell tricks.
- Optional: Integrates physical-key or password protection.

---

## 🧠 Philosophy

**"Don’t just defend. Weaponize your defense."**

PhantomShield shifts the meta from passive hardening to active deception. It forces attackers to waste time, pivot harder, or quit — all while giving the defending team absolute control over the battlefield.

---

## Directory structure of source

You can check Structure.md for the more info that.

---

## 🧪 Intended Use

- Competitive CTF blue team challenges (HackTheBox, NCL, collegiate events)
- Educational cybersecurity simulations
- Real-time anti-pivoting environments

> ❌ Not intended for production environments. This tool is **extreme defense** by design.

---

## ⚠️ Legal

PhantomShield is provided **for educational and competitive use only**. Use outside of authorized CTF environments or without consent of system owners may violate your organisation's AUP and maybe cause system instability.

---

## 🛠 Setup (WIP)

- Requires Windows (10/11 or Server)
- Visual Studio or g++ (MinGW)
- MongoDB URI (if using FirewallBouncer)
- Compile each component or build from the main runner

---

## 🧠 Future Ideas

- Memory scanner / in-memory tampering alerts
- Real-time traffic visualization overlay
- AI-based exploit signature detection
- Kernel-mode driver for even deeper control

---

## 👑 Credits

Developed by [JancoNel](https://github.com/JancoNel)