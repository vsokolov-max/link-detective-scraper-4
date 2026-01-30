# 📦 Deployment Instructions

## Option 1: Use This Repository Directly

### Step 1: Fork/Download
- Download this entire folder
- Or fork on GitHub

### Step 2: Create GitHub Repository
```bash
cd linkdetective-scraper-ready
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/linkdetective-scraper.git
git push -u origin main
```

### Step 3: Deploy to Render
1. Go to https://render.com/
2. Sign up/Login
3. Click "New +" → "Web Service"
4. Connect your GitHub repository
5. Render auto-detects `render.yaml`
6. Click "Create Web Service"
7. Wait 5-10 minutes
8. Done! Your app is live 🎉

## Option 2: Replace Files in Existing Repository

If you already have a repository:

1. **Delete these files** (if they exist):
   - `requirements_streamlit.txt`
   - Old `render.yaml` with apt-get commands

2. **Add/Replace with**:
   - `requirements.txt` (from this folder)
   - `aptfile` (from this folder)
   - `render.yaml` (from this folder)
   - `streamlit_app.py` (from this folder)

3. **Commit and push**:
```bash
git add .
git commit -m "Fix deployment configuration"
git push
```

Render will automatically redeploy!

## ✅ Verification

After successful deployment:

1. Open your app URL (e.g., `https://linkdetective-scraper.onrender.com`)
2. You should see the LinkDetective Scraper interface
3. Test with a real LinkDetective URL
4. Should work!

## 🐛 If Build Fails

### Check these files exist:
- [ ] `requirements.txt` (NOT `requirements_streamlit.txt`)
- [ ] `aptfile`
- [ ] `render.yaml`
- [ ] `streamlit_app.py`

### Check render.yaml:
- [ ] No `apt-get` commands in buildCommand
- [ ] buildCommand is: `pip install -r requirements.txt`
- [ ] startCommand includes correct port: `$PORT`

### Check requirements.txt:
```
streamlit==1.30.0
selenium==4.16.0
pandas==2.1.4
webdriver-manager==4.0.1
```

### Check aptfile:
```
chromium
chromium-driver
```

## 💰 Pricing

### Free Plan
- ✅ Good for testing
- ⚠️ Spins down after 15 min inactivity
- ⚠️ Slow cold starts

### Starter Plan ($7/month)
- ✅ Always on
- ✅ Fast performance
- ✅ Custom domain
- ✅ **Recommended for production**

## 🎯 Success Indicators

✅ Build completes without errors
✅ Service starts successfully  
✅ Can access the URL
✅ Scraping works correctly

## 📞 Need Help?

1. Check Render logs: Dashboard → Your Service → Logs
2. Verify all files match exactly what's in this folder
3. Make sure no extra spaces or typos in filenames

## 🚀 Quick Test

After deployment, test with this URL structure:
```
https://linkdetective.pro?hash=YOUR_HASH
```

Expected flow:
1. Paste URL
2. Click "Start Scraping"
3. Progress bar appears
4. Data loads
5. Download CSV button appears
6. Success! 🎉

---

**Total deployment time: ~10 minutes**
**Difficulty: Easy** ⭐
**Cost: Free or $7/month**
