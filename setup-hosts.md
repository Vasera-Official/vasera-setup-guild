# Setup Local Subdomains

To enable subdomain isolation for local development, you need to add these entries to your Windows hosts file:

## Hosts File Location
`C:\Windows\System32\drivers\etc\hosts`

## Required Entries
Add these lines to the hosts file:

```
127.0.0.1 admin.localhost
127.0.0.1 school.localhost
```

## Instructions

1. **Open Command Prompt or PowerShell as Administrator**
2. **Edit the hosts file** (you can use notepad):
   ```powershell
   notepad C:\Windows\System32\drivers\etc\hosts
   ```
3. **Add the two lines** at the end of the file:
   ```
   127.0.0.1 admin.localhost
   127.0.0.1 school.localhost
   ```
4. **Save the file** (you may need admin permissions)
5. **Restart your browsers** or flush DNS cache:
   ```powershell
   ipconfig /flushdns
   ```

## Alternative Method

You can also run this PowerShell command as Administrator to add the entries automatically:

```powershell
Add-Content -Path "C:\Windows\System32\drivers\etc\hosts" -Value "`n127.0.0.1 admin.localhost`n127.0.0.1 school.localhost"
```

## Verification

After setting up, you should be able to access:
- Admin app: http://admin.localhost:3005
- School app: http://school.localhost:3004
- API server: http://localhost:3000

## Starting the Development Servers

1. **API Server:**
   ```bash
   cd vasera-api
   bun run dev
   ```

2. **Admin App:**
   ```bash
   cd vasera-admin
   bun run dev
   ```

3. **School App:**
   ```bash
   cd vasera-school
   bun run dev
   ```

The subdomain isolation will ensure that cookies are properly isolated between admin and school applications.