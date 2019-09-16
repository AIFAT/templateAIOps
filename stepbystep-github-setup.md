# Step by Step Github Setup Guide

This guide is intended to provide guidance on setting up a github repo for your data science work and making it as easy as possible to set up what is needed while not missing items that will help your projects. This includes configuring your github repo, files to make it easier to set up devops and more.
This guide starts after you've hit the create button on github.

##Table of Contents

1. Set up github team
1. Setup privs read/write/admin
    - impacts who can approve pr
1. Edit Contributing.md
    Decide Branching policy
1. set up labels
1. Create pr and issue templates
    - optional templates
    - in .github/ISSUE_TEMPLATE.md
    - in .github/PULL_REQUEST_TEMPLATE.md
    - in .github/ISSUE_TEMPLATE/
1. Repo stats
1. Helpful Github Commands

- required status checks
- license
- labels
- release strategy
- when someone contributes code to project, add to authors.md

- trick to avoid pushing to master by accident (usually when you intend to push to your own branch):
git config branch.master.pushRemote no_push

## Helpful Github Commands

if you accidently push something:
git revert <commit hash>