# GoDaddy DNS Setup for xslaiacacademy.com

## 🎯 Goal
Point **xslaiacacademy.com** to GitHub Pages

---

## 📋 Step-by-Step Instructions

### **Step 1: Log into GoDaddy**
1. Go to https://www.godaddy.com
2. Sign in
3. Go to **My Products**
4. Find **xslaiacacademy.com**
5. Click **DNS** (or **Manage DNS**)

---

### **Step 2: Delete Existing Records (if any)**

Look for these record types and **DELETE THEM**:
- Any existing **A records** pointing to `@`
- Any existing **CNAME record** for `www`
- Any **parked domain** or **forwarding** records

⚠️ **Keep these if they exist:**
- Email-related records (MX, TXT for email)
- Any records you're using for other services

---

### **Step 3: Add GitHub Pages A Records**

Click **Add Record** and create **4 separate A records**:

#### Record 1
- **Type:** A
- **Name:** @ (or leave blank)
- **Value:** `185.199.108.153`
- **TTL:** 600 seconds (or 1 hour)
- Click **Save**

#### Record 2
- **Type:** A
- **Name:** @ (or leave blank)
- **Value:** `185.199.109.153`
- **TTL:** 600 seconds
- Click **Save**

#### Record 3
- **Type:** A
- **Name:** @ (or leave blank)
- **Value:** `185.199.110.153`
- **TTL:** 600 seconds
- Click **Save**

#### Record 4
- **Type:** A
- **Name:** @ (or leave blank)
- **Value:** `185.199.111.153`
- **TTL:** 600 seconds
- Click **Save**

---

### **Step 4: Add WWW CNAME Record**

Click **Add Record**:

- **Type:** CNAME
- **Name:** www
- **Value:** `iambarabbas.github.io`
- **TTL:** 600 seconds (or 1 hour)
- Click **Save**

---

## ✅ When You're Done, Your DNS Should Look Like This:

```
TYPE    NAME    VALUE                   TTL
────────────────────────────────────────────────
A       @       185.199.108.153         600
A       @       185.199.109.153         600
A       @       185.199.110.153         600
A       @       185.199.111.153         600
CNAME   www     iambarabbas.github.io   600
```

---

## ⏱️ Step 5: Wait for DNS Propagation

- **Minimum:** 10 minutes
- **Maximum:** 48 hours
- **Typical:** 1-2 hours

### Check Status:
Go to https://dnschecker.org and enter `xslaiacacademy.com`

When you see the GitHub IPs showing up globally, you're good!

---

## 🔒 Step 6: Enable HTTPS in GitHub

1. Go to https://github.com/iambarabbas/xsl-ai-academy/settings/pages
2. Wait until DNS propagates
3. Check the box: **"Enforce HTTPS"**
4. GitHub will automatically provision an SSL certificate (takes ~5 min)

---

## 🧪 Testing

After DNS propagates, test these URLs:

- ✅ http://xslaiacacademy.com (should redirect to HTTPS)
- ✅ https://xslaiacacademy.com (should work)
- ✅ http://www.xslaiacacademy.com (should redirect to HTTPS non-www)
- ✅ https://www.xslaiacacademy.com (should work)

All should show your workshop landing page!

---

## 🆘 Troubleshooting

### "Site can't be reached"
- DNS hasn't propagated yet → Wait another hour
- Check dnschecker.org → Not all regions showing GitHub IPs yet

### "Not secure" warning
- HTTPS not enabled yet in GitHub → Wait for DNS, then check "Enforce HTTPS" in GitHub settings

### "404 - There isn't a GitHub Pages site here"
- CNAME file missing → I already added it, should work after DNS propagates
- Custom domain not set in GitHub → Go to repo settings > Pages > enter `xslaiacacademy.com`

### Old site still showing
- Browser cache → Hard refresh (Cmd+Shift+R on Mac, Ctrl+Shift+R on Windows)
- DNS cache → Wait longer or flush DNS (`sudo dscacheutil -flushcache` on Mac)

---

## 📞 Need Help?

If you run into issues:
1. Take a screenshot of your GoDaddy DNS settings
2. Run `dig xslaiacacademy.com` in terminal and share output
3. I'll help debug!

---

**All files already updated to use xslaiacacademy.com! Just need to set up DNS now.** 🚀
