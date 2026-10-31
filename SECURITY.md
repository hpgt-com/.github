## If a push is blocked because of a secret

Push protection stopped the push because a commit contains something that looks like a secret.

1. Do not bypass the block unless the value is a test value or a false positive.
2. Remove the secret from the commit. If it is in the latest commit, edit the file and run
   `git commit --amend`. If it is further back, use `git rebase -i` and edit the commit.
3. If the secret was ever pushed or shared anywhere, treat it as leaked: revoke it and create a new one.
4. Store the new secret in a GitHub environment limited to `main`, never in the code.
