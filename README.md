# Renovate Git URLs

## Current behavior

Dependencies defined in `package.json` as a Git URL (e.g. `https://github.com/mui-org/material-ui#master`) are not updated by Renovate.

## Expected behavior

Renovate should update the resolved version to the last commit hash in the specified branch.

Currently, these dependencies are skipped with the `unversioned-reference` reason.

```json
{
  "config": {
    "npm": [
      {
        "packageFile": "package.json",
        "deps": [
          {
            "depType": "dependencies",
            "depName": "@material-ui/monorepo",
            "currentValue": "https://github.com/mui-org/material-ui#master",
            "skipReason": "unversioned-reference",
            "prettyDepType": "dependency",
            "depIndex": 0,
            "updates": []
          }
        ]
      }
    ]
  }
}     
```
