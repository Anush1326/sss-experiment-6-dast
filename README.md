# SSS Experiment 6 — DAST using OWASP ZAP

A small import-ready GitHub repository for demonstrating Dynamic Application Security Testing (DAST) using GitHub Actions and OWASP ZAP.

## What it does

1. Starts a small static demo website on the GitHub-hosted Ubuntu runner.
2. Runs the OWASP ZAP Baseline scanner against that local website.
3. Shows the scan logs in the repository's Actions tab.

## Import it into your GitHub account

### Option A — Upload the ZIP contents to a new repository
1. Create a new repository on https://github.com/new (choose a name such as `sss-experiment-6-dast`).
2. Download and extract this ZIP on your computer.
3. In the new GitHub repository, choose **Add file → Upload files**.
4. Upload `index.html`, `README.md`, and the `.github` folder (make sure `.github/workflows/dast-pipeline.yml` is preserved).
5. Commit the files to the `main` branch.
6. Open **Actions** and select the latest **DevSecOps Automated DAST Pipeline** run.

### Option B — Push with Git
Extract the ZIP, open a terminal in the extracted folder, and run:

```bash
git init
git branch -M main
git add .
git commit -m "Add OWASP ZAP DAST experiment"
git remote add origin https://github.com/YOUR-USERNAME/sss-experiment-6-dast.git
git push -u origin main
```

Replace `YOUR-USERNAME` with your GitHub username. Create the empty repository on GitHub first.

## Notes

- The workflow runs on pushes and pull requests targeting `main`, and can also be started manually from **Actions → DevSecOps Automated DAST Pipeline → Run workflow**.
- This uses ZAP's **Baseline** scan, which is intended for passive checks. It is not a guarantee that the application is secure.
- The demo is a static training page. For a real project, change the workflow to start your app and scan its actual local URL.
- If GitHub Actions is disabled for the repository, enable it in the repository's Actions settings.
