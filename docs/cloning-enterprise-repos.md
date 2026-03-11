# Cloning SeattleU WebOps Enterprise Repositories

This guide explains how to correctly clone repositories from the SeattleU WebOps GitHub Enterprise organization.

The WebOps repository structure is designed to separate CMS artifacts, compiled applications, and platform tooling to maintain a scalable and maintainable development environment.

---

# Local Directory Structure

All enterprise repositories should be cloned into the following base directory:

```
~/repos/enterprise/webops
```

Example local architecture:

```
enterprise/webops
├── .github
├── cms
│   └── t4
│       ├── components
│       ├── pagelayout
│       └── compiled-apps
├── platform
```

---

# SSH Configuration

Enterprise repositories must be cloned using the SeattleU SSH identity.

Example SSH configuration:

```
Host github-su
  HostName github.com
  User git
  IdentityFile ~/.ssh/id_ed25519_su_chimenti
```

This ensures the correct GitHub account is used when interacting with the SeattleU WebOps organization.

---

# Cloning Component Repositories

TerminalFour content types live in the **components** directory.

Example:

```
cd ~/repos/enterprise/webops/cms/t4/components

git clone git@github-su:seattleu-webops/cms-t4-8084-program-faq.git
```

Example structure after cloning:

```
components
└── cms-t4-8084-program-faq
```

---

# Cloning Page Layout Repositories

Page layout repositories should be cloned into the **pagelayout** directory.

Example:

```
cd ~/repos/enterprise/webops/cms/t4/pagelayout

git clone git@github-su:seattleu-webops/cms-t4-6907517-su-website-2023-full-width.git
```

---

# Cloning Compiled Applications

Applications compiled outside the CMS should be cloned into the **compiled-apps** directory.

Example:

```
cd ~/repos/enterprise/webops/cms/t4/compiled-apps

git clone git@github-su:seattleu-webops/be-legendary-app.git
```

---

# Cloning Platform Tools

Infrastructure and automation tools should be cloned into the **platform** directory.

Example:

```
cd ~/repos/enterprise/webops/platform

git clone git@github-su:seattleu-webops/t4-api-toolkit.git
```

---

# Verify Repository Origin

After cloning a repository, verify that the correct SSH identity is being used.

Run:

```
git remote -v
```

Expected output:

```
origin  git@github-su:seattleu-webops/<repository>.git
```

This confirms that the `github-su` SSH alias is being used.

---

# Important Notes

• Always clone repositories using the `github-su` SSH alias.
• Do not clone enterprise repositories using the default GitHub SSH configuration.
• All repositories should be placed in their appropriate directories within the WebOps architecture.

---

# Maintained By

Seattle University
Web Operations Team
