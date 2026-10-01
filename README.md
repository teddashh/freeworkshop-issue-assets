# freeworkshop-issue-assets

**English** · [繁體中文](README.zh-TW.md)

Screenshots attached to GitHub issues that the 自由工坊 Discord helper bot files on behalf of community members.

**Project page:** https://teddashh.github.io/freeworkshop-issue-assets/

When someone reports a problem in the 自由工坊 Discord, the helper bot drafts a GitHub issue. After the reporter or an admin confirms the draft in Discord, the bot files the issue, commits the attached screenshots here, and links them from the issue. Discord CDN attachment links expire, so the images need a permanent home.

## Layout

```
<owner>/<repo>/<YYYY-MM>/<draft-id>-<n>.<ext>
```

- `<owner>/<repo>`: the repository the issue was filed in
- `<YYYY-MM>`: year and month
- `<draft-id>`: the ID of the Discord draft
- `<n>`: the screenshot number within that draft

Issues link to the files through `raw.githubusercontent.com` URLs on the `main` branch.

## Privacy

- Metadata (EXIF) is stripped before upload.
- The repository is public, so a screenshot becomes public once its draft is confirmed. Check what a screenshot shows before you confirm.
- The project page is built from `site/` only. It never publishes the stored images.

## Removing an image

If a screenshot shows personal information or a secret:

1. If a password, token, or key is visible, rotate it first. Deleting the image does not undo the exposure.
2. Ask an admin in the 自由工坊 Discord. If you are not in the Discord, open an issue in this repository. Name the issue and the screenshot number, or the file path; do not attach the image again.
3. The maintainer deletes the file here and edits the issue to remove the link.

Deleting the file from `main` breaks the image link in the issue, but older commits still contain the file until the Git history is rewritten.

## What is in this repository

Images only. The bot's code is not here. `site/` and `.github/workflows/pages.yml` build the project page.
