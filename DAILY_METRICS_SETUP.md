# 🔥 DAILY GITHUB METRICS AUTOMATION SETUP

Follow these **exact steps** to get your GitHub Metrics running automatically every day like virajchandra51's profile!

## 🚀 Step-by-Step Setup Guide

### 1️⃣ Create Personal Access Token

1. Go to [GitHub Settings → Developer settings → Personal access tokens (classic)](https://github.com/settings/tokens)
2. Click **"Generate new token (classic)"**
3. **Token Name:** `GitHub Metrics Token`
4. **Expiration:** `No expiration` (or 1 year)
5. **Select these scopes:**
   ```
   ✅ repo (Full control of private repositories)
   ✅ read:user (Read user profile data)
   ✅ read:org (Read organization membership)
   ✅ read:project (Read project boards)
   ```
6. Click **"Generate token"**
7. **COPY THE TOKEN** - you won't see it again!

### 2️⃣ Add Token to Repository Secrets

1. Go to your repository: `https://github.com/codewithgarry/codewithgarry`
2. Click **Settings** → **Secrets and variables** → **Actions**
3. Click **"New repository secret"**
4. **Name:** `METRICS_TOKEN`
5. **Secret:** Paste your personal access token
6. Click **"Add secret"**

### 3️⃣ Enable GitHub Actions

1. Go to your repository **Actions** tab
2. If you see a message about workflows, click **"I understand my workflows, go ahead and enable them"**
3. Find the **"Metrics"** workflow
4. Click **"Enable workflow"** if needed

### 4️⃣ Test Manual Run

1. Go to **Actions** → **Metrics** workflow
2. Click **"Run workflow"** → **"Run workflow"**
3. Wait 2-3 minutes for completion
4. Check if `github-metrics.svg` appears in your repository root

## ⏰ Automated Schedule

Your metrics will automatically update:

- **Daily at 12:00 PM IST** (6:30 AM UTC)
- **On every push** to main/master branch  
- **Manual trigger** available anytime

## ✅ Verification Checklist

After setup, verify these items:

- [ ] Personal Access Token created with correct scopes
- [ ] `METRICS_TOKEN` secret added to repository
- [ ] GitHub Actions enabled for the repository
- [ ] Metrics workflow shows up in Actions tab
- [ ] Manual test run completes successfully
- [ ] `github-metrics.svg` file appears in repository root
- [ ] Workflow is scheduled to run daily

## 🔧 Troubleshooting

### Common Issues:

1. **Workflow doesn't run:**
   - Check if GitHub Actions are enabled
   - Verify the repository is public or you have GitHub Pro
   - Ensure the workflow file is in `.github/workflows/`

2. **Token errors:**
   - Regenerate token with all required scopes
   - Double-check secret name is exactly `METRICS_TOKEN`
   - Ensure token hasn't expired

3. **Empty or broken SVG:**
   - Verify username is `codewithgarry` in workflow
   - Check if token has `repo` scope for private repos
   - Try manual run to see detailed error logs

4. **Schedule not working:**
   - GitHub may delay scheduled workflows during high traffic
   - Free accounts have lower priority for scheduled runs
   - Manual triggers always work immediately

## 📁 Expected Files

After successful setup, you'll have:

```
your-repo/
├── .github/
│   └── workflows/
│       ├── metrics.yml          # Main metrics workflow
│       ├── metrics-simple.yml   # Simplified version
│       └── devops-metrics.yml   # DevOps-focused metrics
├── github-metrics.svg           # Generated daily
├── devops-metrics.svg          # Generated daily  
└── README.md                   # Your profile
```

## 🎯 Next Steps

1. **Complete the setup** following steps 1-4
2. **Wait for first automated run** (next day at 12 PM IST)
3. **Check Actions tab** to see run history like virajchandra51
4. **Enjoy automated daily metrics!** 🎉

## 🌟 Pro Tips

- **Star the metrics repository** to show support: [lowlighter/metrics](https://github.com/lowlighter/metrics)
- **Customize plugins** by editing the workflow files
- **Add multiple metrics files** for different focuses
- **Use different schedules** for different metrics

---

**🔥 Once configured, your metrics will update automatically every single day, just like virajchandra51's profile!**