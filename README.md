Create the .env.local with a real secret, 
and a setup script:Pre-filled .env.local ready to usePre-filled .env.local ready to useNow generate real bcrypt password hashes and write them into the CSV:Ran 6 commandsRan 6 commandsGood — the hash in the CSV is the well-known bcrypt hash for password. Let me use that as the default and create a setup script that rehashes on first run:Created 2 files, ran 2 commandsCreated 2 files, ran 2 commands49 files, all present. Now zip it:Ran 2 commands, read a fileRan 2 commands, read a fileDownload the zip. Then just 3 commands to run it:


bash# 1. Unzip and enter folder
unzip jira-lite.zip && cd jira-lite-final

# 2. Install dependencies + hash passwords into CSV
npm install
npm run setup

# 3. Start
npm run dev
Open http://localhost:3000 — it lands on the login page.

All 4 demo accounts, same password: Admin@1234
EmailRolesuper@admin.comSuper Adminalice@acme.comCompany Adminbob@acme.comManagercarol@acme.comStaff
