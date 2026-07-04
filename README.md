# Blueprint Install — LashariGamer Script

Ek simple aur fast auto-installer script jo **Pterodactyl Panel** par **Blueprint Framework** aur uske addons ko automatically install kar deta hai — bina manually har command copy-paste kiye.

Made By **LashariGamer**

---

## 📋 Requirements (Zaroori Cheezein)

Script chalane se pehle ye cheezein already ready honi chahiye:

- Ek VPS (Ubuntu/Debian based)
- **Pterodactyl Panel** already installed ho, aur uska path `/var/www/pterodactyl` ho
- `sudo` / root access
- Internet connection

> ⚠️ Agar Pterodactyl Panel install nahi hai, toh pehle panel install karein, phir ye script chalayein.

---

## 🚀 Installation (Single Command)

Bas ek command run karni hai apne VPS ke terminal mein — koi `git clone` karne ki zaroorat nahi:

```bash
bash <(curl -fsSL https://raw.githubusercontent.com/atifqmi-max/blueprint-install/main/install.sh)
```

Command run karne ke baad:

1. Script ek banner show karega — **LashariGamer Script**
2. Ek confirmation puchega:
   ```
   Continue Installing (y/n):
   ```
   - `y` dabao → Installation shuru ho jayegi
   - `n` dabao → Script exit ho jayega, kuch install nahi hoga

---

## ⚙️ Ye Script Kya Karta Hai

Script pura process automatic chalata hai:

### Step 1 — Blueprint Framework Setup
- Zaroori packages install karta hai (`curl`, `wget`, `unzip`, `git`, `gnupg`, `zip`)
- Blueprint Framework ka latest release download karta hai
- NodeJS (v22) aur Yarn setup karta hai
- Pterodactyl directory mein `yarn install` chalata hai
- `.blueprintrc` config file banata hai (webserver user set karta hai)
- `blueprint.sh` ko permission deta hai aur run karta hai

### Step 2 — Addon Installer
- Blueprint addon installer script automatically run karta hai:
  ```bash
  bash <(curl -fsSL https://raw.githubusercontent.com/hopingboyz/blueprint/main/addon-installer.sh)
  ```

### Step 3 — Completion
- Aakhir mein banner phir se show hota hai:
  ```
  LashariGamer Script
       Made By LashariGamer

  Thanks For Using This Script
  ```

---

## 📁 Files

| File          | Description                                  |
|---------------|-----------------------------------------------|
| `install.sh`  | Main installer script — sab kuch automatic karta hai |

---

## ❓ FAQ

**Q: Kya mujhe manually koi command chalani hogi?**
Nahi, sirf ek command chalani hai. Baqi sab script khud handle karega.

**Q: Agar meri Pterodactyl directory `/var/www/pterodactyl` nahi hai?**
Script mein `PTERODACTYL_DIRECTORY` variable define hai — agar path different hai, `install.sh` file mein wo variable edit kar lein.

**Q: Kya ye script safe hai?**
Script sirf official Blueprint Framework release aur ek third-party addon-installer script use karta hai. Use karne se pehle script ka content khud bhi review karlein.

**Q: Installation beech mein fail ho gayi, kya karun?**
Ensure karein ke Pterodactyl already installed hai, `sudo` access available hai, aur internet connection stable hai. Phir dobara command run karein.

---

## 📜 Credits

- **Script by:** LashariGamer
- **Blueprint Framework:** [BlueprintFramework/framework](https://github.com/BlueprintFramework/framework)
- **Addon Installer:** [hopingboyz/blueprint](https://github.com/hopingboyz/blueprint)

---

### Thanks For Using This Script ❤️
