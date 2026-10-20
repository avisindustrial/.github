<!--
Title format: <type>(<optional scope>): <summary> (AB#1234 | CASE-00001234)
Example:      feat(tools): add labor efficiency tool (AB#4521)
-->

## Work item

<!-- Azure Boards: "Fixes AB#1234" closes the item on merge; "AB#1234" only links it.
     Help desk case: "CASE-00001234". Also add this PR's link to the case. -->

Fixes AB#

## Summary

<!-- What changed and why. -->

## Testing

<!-- How you verified it. List new or updated tests. -->

- [ ] Unit tests added or updated
- [ ] Tested locally
- [ ] Bug fix includes a test that fails without the fix

## Deployment and rollback

<!-- Config, secrets, migrations or ordering to know about, and how to roll back. "None" is fine. -->

## Screenshots or sample output

<!-- Optional. Remove if not relevant. -->

## Checklist

- [ ] Title follows Conventional Commits and ends with the work-item reference
- [ ] No secrets, credentials or real business data in code or fixtures
- [ ] Docs and README updated if behaviour changed
- [ ] Breaking changes marked with `!` or a `BREAKING CHANGE:` footer
