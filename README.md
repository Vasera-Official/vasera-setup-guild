# Vasera Dev Setup Guild

For sub domain setup visit setup-host.md 
Make sure to have concurrently installed globally

```bash
bun add concurrently
```

## Folder sturcture

This is the folder structure of the project

```
.
├── vasera-api
├── vasera-school
├── vasera-setup-guild
├── packege.json


copy the packege.json to the root folder
```
{
    "name": "agency-vasera",
    "scripts": {
        "email": "cd ./vasera-api; bun run dev:email",
        "dev:vasera-school": "cd ./vasera-school; bun run dev",
        "dev:vasera-api": "cd ./vasera-api; bun run dev",
        "dev:all": "concurrently --kill-others-on-fail --names school,api --prefix-colors green,pink \"bun run dev:vasera-school\" \"bun run dev:vasera-api\"",
        "dev": "bun run dev:all"
    }
}
```

## Running the project
To run the project, use the following command:

```bash
bun run dev
```
This will start both the Vasera School and Vasera API servers concurrently.
The website will open automatically in your default web browser.