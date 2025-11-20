# 🚀 Deployment Checklist - Movie Explorer

## ✅ Status: Ready to Deploy!



## STEP 1: Get TMDB API Key ⏳

1. **Sign up for TMDB account:**
   - Go to: https://www.themoviedb.org/signup
   - Fill in your details (free, no payment needed)
   - Verify your email

2. **Get API Key:**
   - Go to: https://www.themoviedb.org/settings/api
   - Click "Create" or "Request an API Key"
   - Choose "Developer" option
   - Fill in the form (can use dummy URL like http://localhost:3000)
   - Copy your API key (looks like: `abc123def456ghi789jk....`)
   - **Save it somewhere safe** - you'll need it for Vercel!

---

## STEP 2: Create GitHub Repository ⏳

1. **Go to GitHub:**
   - URL: https://github.com/new

2. **Fill in details:**
   - Repository name: `movie-explorer`
   - Description: `Movie Explorer web app - search movies, view details, save favorites`
   - Visibility: **Public** (required for free Vercel deployment)
   - **DO NOT** check any of these:
     - ❌ Add a README file
     - ❌ Add .gitignore
     - ❌ Choose a license
   
3. **Click "Create repository"**

---

## STEP 3: Push Code to GitHub ⏳

**Run these commands in VS Code terminal:**


```powershell
# Add GitHub as remote 
git remote add origin https://github.com/Gunjan-D/movie-explorer.git

# Push your code
git push -u origin main
```

**If you get an error about authentication:**
- GitHub might ask you to log in
- Use GitHub Desktop or Personal Access Token
- Or authenticate via browser when prompted

---

## STEP 4: Deploy to Vercel ⏳

1. **Go to Vercel:**
   - URL: https://vercel.com

2. **Sign Up / Log In:**
   - Click "Sign Up" or "Login"
   - Choose "Continue with GitHub"
   - Authorize Vercel to access your GitHub account

3. **Create New Project:**
   - Click "Add New..." → "Project"
   - You'll see a list of your GitHub repositories
   - Find and click on `movie-explorer`
   - Click "Import"

4. **Configure Project:**
   - **Framework Preset:** Next.js (should auto-detect)
   - **Root Directory:** `./` (leave as default)
   - **Build Command:** (leave default - `npm run build`)
   - **Output Directory:** (leave default - `.next`)

5. **Add Environment Variable (IMPORTANT!):**
   - Click "Environment Variables" section
   - Name: `TMDB_API_KEY`
   - Value: (paste your TMDB API key from Step 1)
   - Click "Add"

6. **Deploy:**
   - Click "Deploy" button
   - Wait 2-3 minutes while Vercel builds your app
   - You'll get a URL like: `https://movie-explorer-xyz123.vercel.app`

7. **Test Your App:**
   - Click on the deployment URL
   - Try searching for a movie (e.g., "Inception")
   - Click on a movie to see details
   - Add to favorites with rating and note
   - Verify favorites persist after refresh

---

