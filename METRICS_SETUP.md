# GitHub Metrics Setup Guide for codewithgarry

This repository uses [lowlighter/metrics](https://github.com/lowlighter/metrics) to generate comprehensive GitHub analytics SVGs automatically.

## 🚀 Quick Setup

### Step 1: Create Personal Access Token

1. Go to [GitHub Settings → Developer settings → Personal access tokens](https://github.com/settings/tokens)
2. Click "Generate new token (classic)"
3. Give it a name: `GitHub Metrics Token`
4. Select scopes:
   - ✅ `public_repo` (for public repositories)
   - ✅ `read:user` (to read user profile)
   - ✅ `read:org` (to read organization data)
   - ✅ `read:project` (to read project boards)

### Step 2: Add Token to Repository Secrets

1. Go to your repository → Settings → Secrets and variables → Actions
2. Click "New repository secret"
3. Name: `METRICS_TOKEN`
4. Value: Paste your personal access token
5. Click "Add secret"

### Step 3: Enable GitHub Actions

1. Go to your repository → Actions tab
2. If prompted, click "I understand my workflows, go ahead and enable them"
3. The workflows will run automatically based on the schedule

## 📊 Generated Metrics

The setup creates two comprehensive metrics files:

### 1. `github-metrics.svg` - General Analytics
- 📅 Full-year commit calendar
- 🈷️ Programming languages analysis
- 🎖️ GitHub achievements
- 🌟 Recently starred repositories
- 💬 Discussions participation
- 🧑‍🤝‍🧑 Followers and following
- 📈 Recent activity

### 2. `devops-metrics.svg` - DevOps Focus
- 💻 Coding habits and patterns
- 🏅 Development consistency
- 💡 Code insights and statistics
- 🎯 Notable contributions
- 📊 Wakatime integration (if connected)
- 🗂️ Active repositories overview

## ⚙️ Customization

### Modify Metrics Configuration

Edit `.github/workflows/metrics.yml` or `.github/workflows/devops-metrics.yml` to:

- Add/remove plugins
- Change update schedule
- Modify appearance
- Include/exclude specific data

### Available Plugins

- `plugin_isocalendar` - Commit calendar
- `plugin_languages` - Programming languages
- `plugin_achievements` - GitHub achievements
- `plugin_habits` - Coding habits
- `plugin_notable` - Notable contributions
- `plugin_wakatime` - Time tracking
- `plugin_code` - Code metrics
- And many more...

## 🔄 Update Schedule

- **General Metrics**: Daily at 12:00 PM IST
- **DevOps Metrics**: Daily at 6:00 PM IST
- **Manual Trigger**: Available via Actions tab

## 🎨 Display in README

The metrics are integrated into your README.md in collapsible sections:

```markdown
<details>
<summary><b>📈 Detailed GitHub Metrics</b></summary>
<br>
<img src="github-metrics.svg" alt="GitHub Metrics" width="100%"/>
</details>
```

## 🛠️ Troubleshooting

### Common Issues

1. **Metrics not generating**: Check if `METRICS_TOKEN` secret is set correctly
2. **Empty SVG files**: Ensure token has proper scopes
3. **Workflow fails**: Check Actions tab for detailed error logs

### Debug Mode

Add to workflow for debugging:
```yaml
config_debug: yes
```

## 📚 Advanced Configuration

For advanced features like:
- Custom plugins
- Multiple metrics files
- Different themes
- Wakatime integration

Refer to the [official documentation](https://github.com/lowlighter/metrics).

## 🎯 Matrix Theme Integration

The metrics SVGs are designed to complement your Matrix-themed profile:
- Dark background compatible
- Green accent colors
- Professional DevOps focus
- Consistent with overall aesthetic

---

**Note**: After first setup, it may take a few minutes for the initial metrics to generate. The SVG files will appear in your repository root after the first successful workflow run.