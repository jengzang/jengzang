# GitHub Profile Setup Instructions

## ✅ Files Created

The following files have been created in your project:

1. **README.md** - Main profile page with all features
2. **.github/workflows/snake.yml** - Snake animation workflow
3. **.github/workflows/blog-posts.yml** - Blog posts feed workflow
4. **.github/workflows/waka-readme.yml** - WakaTime stats workflow

## 📋 Next Steps

### Step 1: Create GitHub Repository

1. Go to https://github.com/new
2. **Repository name MUST be**: `jengzang` (same as your username)
3. Set visibility to **Public**
4. **DO NOT** initialize with README (we already have one)
5. Click "Create repository"

### Step 2: Push Files to GitHub

Run these commands in your terminal:

```bash
cd C:\Users\joengzaang\CodeProject\githubHomePage
git init
git add .
git commit -m "Initial commit: GitHub profile page

Co-Authored-By: Claude Sonnet 4.5 <noreply@anthropic.com>"
git branch -M main
git remote add origin https://github.com/jengzang/jengzang.git
git push -u origin main
```

### Step 3: Enable GitHub Actions

1. Go to your repository: https://github.com/jengzang/jengzang
2. Click on **Settings** tab
3. In the left sidebar, click **Actions** → **General**
4. Under "Workflow permissions", select **Read and write permissions**
5. Check **Allow GitHub Actions to create and approve pull requests**
6. Click **Save**

### Step 4: Enable GitHub Pages (for Snake Animation)

1. In your repository, go to **Settings** → **Pages**
2. Under "Source", select **Deploy from a branch**
3. Under "Branch", select **output** branch (will appear after first workflow run)
4. Click **Save**

### Step 5: Setup WakaTime (Optional but Recommended)

1. **Create WakaTime Account**:
   - Go to https://wakatime.com/signup
   - Sign up with GitHub or email

2. **Install WakaTime Plugin**:
   - For VS Code: https://marketplace.visualstudio.com/items?itemName=WakaTime.vscode-wakatime
   - For other IDEs: https://wakatime.com/plugins
   - Enter your API key when prompted

3. **Get API Key**:
   - Go to https://wakatime.com/settings/api-key
   - Copy your API key

4. **Add to GitHub Secrets**:
   - Go to your repository: https://github.com/jengzang/jengzang
   - Click **Settings** → **Secrets and variables** → **Actions**
   - Click **New repository secret**
   - Name: `WAKATIME_API_KEY`
   - Value: Paste your WakaTime API key
   - Click **Add secret**

### Step 6: Setup Spotify Widget (Optional)

1. Go to https://spotify-github-profile.vercel.app/api/view
2. Click **Login with Spotify**
3. Authorize the application
4. Copy the generated URL (looks like: `https://spotify-github-profile.vercel.app/api/view?uid=YOUR_ID...`)
5. Edit README.md and replace `YOUR_SPOTIFY_ID` with your actual Spotify user ID

To find your Spotify user ID:
- Open Spotify → Click your profile → Share → Copy link to profile
- Extract the ID from the URL (e.g., `spotify:user:YOUR_ID`)

### Step 7: Verify Blog RSS Feed

Your blog is at https://www.yzup.top/. The workflow will try these RSS feed URLs:
- https://www.yzup.top/rss.xml
- https://www.yzup.top/feed.xml
- https://www.yzup.top/atom.xml

If your blog uses a different RSS URL, edit `.github/workflows/blog-posts.yml` and update the `feed_list` parameter.

### Step 8: Trigger Workflows Manually

1. Go to **Actions** tab in your repository
2. You'll see three workflows:
   - **Generate Snake**
   - **Latest Blog Posts**
   - **WakaTime Stats**
3. Click on each workflow
4. Click **Run workflow** → **Run workflow**
5. Wait for them to complete (green checkmark)

### Step 9: Verify Your Profile

1. Visit https://github.com/jengzang
2. Check that all sections display correctly:
   - ✅ Animated typing header
   - ✅ About Me section
   - ✅ Tech stack badges
   - ✅ GitHub statistics (4 widgets)
   - ✅ Recent activity graph
   - ✅ Social links
   - ✅ Visitor counter

3. After workflows run:
   - ✅ Snake animation (appears after first run)
   - ✅ WakaTime stats (appears after setup + first run)
   - ✅ Blog posts (appears if RSS feed is valid)
   - ✅ Spotify widget (appears after setup)

## 🎨 Customization Options

### Change Color Theme

All widgets use the **radical** theme (pink/purple). To change:

Edit README.md and replace `theme=radical` with:
- `theme=dark` - Dark gray
- `theme=tokyonight` - Blue/purple
- `theme=dracula` - Purple/pink
- `theme=github_dark` - GitHub dark mode
- `theme=gruvbox` - Retro
- `theme=onedark` - Atom-inspired

### Update Personal Information

Edit README.md to update:
- About Me section
- Tech stack badges
- Social links
- Any other content

## 🔧 Troubleshooting

### Snake animation not showing
- Wait 24 hours for first scheduled run, or trigger manually
- Check that GitHub Pages is enabled with `output` branch
- Verify workflow completed successfully in Actions tab

### WakaTime stats not updating
- Verify `WAKATIME_API_KEY` is added to repository secrets
- Check that WakaTime plugin is installed and tracking your coding
- Wait 24 hours for first update

### Blog posts not showing
- Verify your blog has a valid RSS feed
- Check workflow logs in Actions tab for errors
- Update feed URL in `.github/workflows/blog-posts.yml` if needed

### Spotify widget not working
- Make sure you completed the authorization at spotify-github-profile.vercel.app
- Update the widget URL in README.md with your actual Spotify user ID
- The widget only shows when you're actively playing music

## 📊 Workflow Schedule

- **Snake Animation**: Runs daily at midnight UTC
- **Blog Posts**: Runs every 6 hours
- **WakaTime Stats**: Runs daily at midnight UTC

You can also trigger any workflow manually from the Actions tab.

## 🎉 You're Done!

Your GitHub profile is now set up with:
- ✨ Animated typing header
- 📊 Real-time GitHub statistics
- 🐍 Contribution snake animation
- 📈 WakaTime coding stats (after setup)
- 🎵 Spotify now playing (after setup)
- 📝 Latest blog posts (if RSS feed works)
- 🌐 Social media links
- 👁️ Visitor counter

Visit https://github.com/jengzang to see your awesome new profile!
