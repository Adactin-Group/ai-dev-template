# New project setup checklist

Complete this on day one for every repository created from `ai-dev-template`.
GitHub copies files from a template, **not settings** — steps 2–4 must be redone.

## 1. Create the repository

- [ ] *Use this template* → *Create a new repository* in the organisation
- [ ] Visibility agreed with the Technical Director (public only if the code may be visible to anyone)
- [ ] Create the integration branch: `git switch -c dev` then `git push -u origin dev`

## 2. Repository settings (Settings → General)

- [ ] Squash merging only; auto-delete head branches; suggest updating PR branches
- [ ] Wikis, Projects and Discussions off unless needed

## 3. Access (Settings → Collaborators and teams)

- [ ] `platform-admins` Admin · `leads` Maintain · `engineers` Write · `security-reviewers` Write
- [ ] No individual (non-team) access

## 4. Security and Actions

- [ ] Dependency graph, Dependabot alerts and security updates on
- [ ] Secret scanning and push protection on
- [ ] Private vulnerability reporting on
- [ ] Actions: workflow permissions read-only; Actions cannot approve PRs; fork PR workflows need approval
- [ ] Branch rulesets for `main` and `dev` applied (see `docs/governance/rulesets.md` once added)

## 5. Replace placeholders

- [ ] `openspec/config.yaml` — project, owners, risk tier, data classification
- [ ] `CLAUDE.md` — project name, purpose, stack, tier
- [ ] `.github/CODEOWNERS` — replace `<org>`; adjust security-sensitive paths
- [ ] `SECURITY.md` — security contact
- [ ] `README.md` — project description

## 6. Developer machines

- [ ] Node.js 20.19+, Git, GitHub CLI, Claude Code installed
- [ ] `npm install -g @fission-ai/openspec@latest`
- [ ] OpenSpec telemetry off: `openspec config set telemetry.enabled false`
- [ ] 2FA on every GitHub account
- [ ] Each developer has read `CLAUDE.md` and the AI acceptable-use rules

## 7. First change

- [ ] First OpenSpec change raised with `/opsx:propose`, reviewed by a human, merged by pull request
