# Guadalupe NHS DTR – Mac app

A stand-alone macOS app (no Chrome/Edge/Safari needed). Same generator, packaged with Electron.

## Get the Mac app (no coding, GitHub builds it for you)

1. Create a GitHub repository and upload **everything in this folder**
   (keep the `.github/workflows` folder: it's what builds the app).
2. Open the repo's **Actions** tab → **Build Mac app** → **Run workflow**.
3. When it turns green (about 5 minutes), open the run and download **GNHS-DTR-mac** at the bottom.
4. Unzip it. Open the `.dmg` that matches your Mac and drag **Guadalupe NHS DTR** into **Applications**:
   - `...-arm64.dmg` for Apple Silicon (M1/M2/M3/M4, any Mac from late 2020 on)
   - `...-x64.dmg` for older Intel Macs
   (Apple menu → About This Mac tells you which chip you have.)

## First time opening (the app is not notarized by Apple)

macOS may say the app can't be verified. This is normal for apps without a paid Apple Developer account.
- Right-click (or Control-click) the app → **Open** → **Open**, or
- System Settings → **Privacy & Security** → scroll down → **Open Anyway**.
- If it still refuses, run in Terminal: `xattr -cr "/Applications/Guadalupe NHS DTR.app"`

You only need to do this once.

## Run / build on your own Mac (optional)

Install Node.js, then in this folder:

    npm install
    npm start              # try it
    npm run build:mac      # makes the .dmg in dist/

## Updating

Replace `app/index.html`, bump `version` in `package.json`, and run the workflow again.
