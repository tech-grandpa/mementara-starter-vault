---
title: Connect a repository
aliases: [Repository onboarding, Add a repository]
tags: [guide, github, getting-started]
---
# Connect a repository

Signing in tells Mementara which GitHub account you use. Repository access is a separate choice: you decide which repositories the Mementara GitHub App may read. An empty list just after sign-in usually means that access has not been granted yet.

The bundled sample works without signing in. To read your own notes, follow these steps in a configured Mementara build. Public App Store and TestFlight distribution are not available yet.

## 1. Prepare your repository

If your notes already live in a GitHub repository, you can use it as it is. Make sure it has at least one committed Markdown (`.md`) or plain-text (`.txt`) note on the branch you intend to read.

To start a new notebook:

1. Open the [Mementara starter vault](https://github.com/tech-grandpa/mementara-starter-vault).
2. Choose **Use this template → Create a new repository**.
3. Choose your account or organization as the owner and give the repository a name, such as `my-notes`.
4. Choose **Private** if your notes should stay private, then create the repository.
5. Edit the sample notes or add your own using GitHub or your usual editor. Commit and push your changes so they are available on GitHub.

Creating a copy does not automatically grant Mementara access to it. Keep personal information out of the public starter repository; add it only to your own private copy.

## 2. Allow Mementara to read it

1. In Mementara, tap **Connect GitHub** and sign in. If you already have a vault open, use **Settings → Connect or replace GitHub vault**.
2. In the repository picker, tap **Choose repositories on GitHub**. You can also open [Mementara's GitHub App installation page](https://github.com/apps/mementara/installations/new).
3. Choose the **account or organization that owns the repository**. This may be different from your personal account. If Mementara is already installed there, choose **Configure**.
4. Under repository access, choose **Only select repositories**. Use **Select repositories** to add the notebook you want to read. Leave any other repositories you still use selected.
5. Review the permissions: Mementara asks for **read-only Contents and Metadata**. Tap **Install** for a new installation or **Save** when changing an existing one.
6. Return to Mementara. If GitHub remains open, tap **Done** to close the browser. The list refreshes when you return; **Refresh repositories** also checks for changes.

Your GitHub account must itself have access to the repository. Allowing the app access does not give your account additional rights.

### Organization approval

GitHub may show **Request** or **Install and request** if an organization owner must approve installation or repository access. Submit the request and wait for approval; repeatedly signing in will not bypass it. If your organization blocks requests, ask its owner to install Mementara for the selected repository. Return to Mementara and refresh after access is approved. Complete your organization's GitHub single sign-on if prompted.

## 3. Download your notebook

1. Select the repository in Mementara. If only one is available, it is selected automatically.
2. Choose the branch containing your notes, usually `main`.
3. Leave **Root folder** empty to include the whole repository. To include only a folder, enter a relative path such as `notes` or `docs/handbook`, without a leading slash.
4. Tap **Download vault** and wait for **Available offline**.
5. Open a note, search for a phrase, then try again in airplane mode.

If you are replacing an existing vault, the button says **Switch vault**. Confirming removes the previous local copy, including its bookmarks and reading progress. Files on GitHub stay unchanged.

## Add another repository later

Open **Settings → Manage allowed repositories**, or **Choose repositories on GitHub** in the picker. Select the owner, open **Configure** if needed, add the new repository under **Only select repositories**, and **Save**. Return to the app and refresh. Then use **Connect or replace GitHub vault** to choose and download it.

Mementara currently reads one downloaded vault at a time. Granting access to several repositories lets you choose between them; it does not download all of them automatically.

## If the list is still empty

- **Check the account.** The account shown in Mementara should match the GitHub account used in the browser. If you signed into the wrong account in Mementara, sign out in Settings and connect the intended account.
- **Check the owner and selection.** Install/configure Mementara on the repository's owner, select that repository and save. Access on your personal account does not cover an organization-owned repository.
- **Check approval.** An organization request must be approved before access appears. If approval is blocked, contact the repository or organization owner.
- **Check the app name.** These instructions use **Mementara**. A developer's Debug build uses the separate **Mementara Development** registration; grants to one do not apply to the other.
- **Refresh while online.** Return to Mementara and tap **Refresh repositories**. A refresh error is shown separately; try again when connected.

Mementara reads your repositories directly from GitHub. It does not need a Mementara account or authentication server, and it cannot edit or push your notes. To update a downloaded notebook, edit and push to GitHub, then refresh in Mementara.

[Back to Getting started](Getting%20started.md) · [Back to Welcome](../Welcome.md)

GitHub's [installation guide](https://docs.github.com/en/apps/using-github-apps/installing-a-github-app-from-a-third-party) explains repository selection and organization approval.
