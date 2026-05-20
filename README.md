# SMS Expense Tracker — Get Your APK in 10 Minutes

No PC setup. No Android Studio. Just GitHub (free) → APK downloads to your phone.

---

## How to get the APK (step by step)

### Step 1 — Create a free GitHub account
Go to https://github.com/signup
- Use any email, create a username and password
- Verify your email

### Step 2 — Create a new repository
1. Click the **+** button (top right) → "New repository"
2. Name it: `expense-tracker`
3. Set to **Public**
4. Click **Create repository**

### Step 3 — Upload this project
1. On your new repo page, click **"uploading an existing file"** link
2. Drag and drop the entire contents of this ZIP (extract first) into the browser
3. Make sure you see ALL these folders uploaded:
   - `.github/workflows/build.yml`
   - `app/src/main/java/...`
   - `app/src/main/AndroidManifest.xml`
   - `build.gradle`, `settings.gradle`, `gradlew`, etc.
4. Scroll down → click **"Commit changes"**

### Step 4 — Watch it build (takes ~5 minutes)
1. Click the **"Actions"** tab at the top of your repo
2. You'll see **"Build APK"** running with a yellow circle ⏳
3. Wait for it to turn green ✅ (about 3–5 minutes)
4. If it turns red ❌ — see Troubleshooting below

### Step 5 — Download your APK
1. Click on the completed **"Build APK"** run
2. Scroll down to **"Artifacts"** section
3. Click **"ExpenseTracker-debug"** to download
4. You'll get a ZIP file containing `app-debug.apk`

### Step 6 — Install on your Android phone
**Send APK to your phone:**
- Email the APK to yourself and open it on your phone, OR
- Save to Google Drive and open on your phone, OR
- Transfer via USB cable

**Install it:**
1. Tap the APK file on your phone
2. If prompted "Install from unknown sources" → tap **Settings** → enable it → go back and install
3. Tap **Install**
4. Done! Find "Expense Tracker" in your app drawer

---

## First time using the app

1. **Open the app** → tap "Allow" when asked for SMS permission
2. **Tap ⚙ Settings** → paste your Anthropic API key → tap Save
   - Get free key at: https://console.anthropic.com
   - New accounts get $5 free credit (~3 months of personal use at ₹3/month)
3. **Tap ⟳ Sync** on the dashboard
4. Wait 10–30 seconds — your bank SMS are being read and categorized
5. Your expense dashboard appears with charts and category breakdown!

---

## What the app does

- **Reads SMS** from HDFC, SBI, ICICI, Axis, Kotak, Paytm + 30 other banks
- **AI categorization** using Claude Haiku — Food, Shopping, Transport, Fuel, etc.
- **Dashboard** — monthly totals, category breakdown with progress bars, KPI cards
- **Transactions** screen — search, filter by bank/category/month/type, tap to see raw SMS
- **Edit categories** — if AI got it wrong, tap ✏ to fix
- **Export CSV** — opens share sheet, save to Google Drive / email / WhatsApp
  - Detailed CSV: every transaction with date, bank, amount, merchant, category
  - Monthly summary: totals per category per month (opens in Excel/Google Sheets)
- **All data local** — stored on your phone only, nothing in any cloud

---

## Troubleshooting GitHub Actions build

**Build failed with red ❌:**
1. Click the failed run → click "build" → scroll to see the error
2. Common fix: make sure ALL files were uploaded including `gradlew` and `gradle/wrapper/gradle-wrapper.jar`

**"Gradle wrapper not found":**
Make sure `gradle/wrapper/gradle-wrapper.jar` was uploaded (it's a binary file, ~29KB)

**APK installs but crashes:**
The API key is empty. Open Settings in the app and add your Anthropic key.

**"No transactions found" after sync:**
Your bank may not be in our sender ID list. Open an issue on your GitHub repo and share your bank name.

---

## Cost summary

| What | Cost |
|------|------|
| GitHub account | Free |
| Building the APK | Free (GitHub Actions minutes) |
| Claude API (AI parsing) | ~₹3/month for ~50 SMS |
| Anthropic signup credit | $5 free = ~3-4 months free |
| App itself | Free, no subscriptions |
