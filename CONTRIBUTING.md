# Contributing

This guide applies to every repository in the `avisindustrial` organization unless the repository has its own `CONTRIBUTING.md`. Members of the organization can find the full standards in the internal software development handbook.

## Before you start

- Every change to a code repository traces back to a work item: an Azure Boards work item or a Transformation Help Desk case. Create or find one first.
- Read the repository's `README.md` for how to build, run and test it locally.

## Branches

`main` is the only long-lived branch. Work on a short-lived branch and merge it through a pull request, ideally within three working days.

Name branches `<type>/<work-item-id>-<short-description>`, all lowercase:

- `type`: `feature`, `fix`, `hotfix`, `chore`, `refactor`, `test`, `docs`, `ci` or `spike`
- `work-item-id`: the Azure Boards ID (`4521`) or the full 8-digit case number with leading zeros (`00007185`), without the `AB#` or `CASE-` prefix
- `short-description`: 2 to 5 hyphenated words

Examples: `feature/4521-labor-efficiency-tool`, `fix/00007185-expired-token-error`

Documentation repositories may use document-type prefixes instead, such as `docs/<slug>` or `adr/<slug>`.

## Pull requests

Pull request titles follow [Conventional Commits](https://www.conventionalcommits.org/) and end with the work-item reference:

```
<type>(<optional scope>): <imperative summary> (AB#<id> | CASE-<8-digit number>)
```

Examples: `feat(tools): add labor efficiency tool (AB#4521)`, `fix(auth): reject expired tokens (CASE-00007185)`

In the description, include:

- The linked work item. Use `Fixes AB#<id>` to close an Azure Boards item on merge. For a help desk case, add the PR link to the case yourself.
- A summary of the change and why it is needed
- How you tested it
- Deployment or rollback notes, if any
- Screenshots or sample output where useful

Pull requests are squash-merged, so the title becomes the commit message on `main`. Mark breaking changes with `!` after the type (`feat!:`) or a `BREAKING CHANGE:` footer.

## Reviews and checks

- All required CI checks must pass before merge.
- Reviewers and code owners are set per repository. Authors cannot approve their own pull requests.
- Resolve every review conversation before merging.
- Every bug fix includes a test that fails without the fix.

## Never commit

- Secrets, tokens, passwords or connection strings. Use the repository's secret store.
- Real production, customer or employee data, including in test fixtures.

If you commit a secret by mistake, treat it as exposed: rotate it immediately and report it as described in [SECURITY.md](SECURITY.md).
