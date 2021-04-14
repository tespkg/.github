


## Overview

This document outlines the git flow for developers working on projects where there is more than 1 active contributer. This does not apply to isolated projects with a single active developer however it is highly reccommended.



## Branches

Branches should be used to isolate developmental code & ensure organised merging & tracking of features and production tags. 

**Required Read: ** https://guides.github.com/introduction/flow/



### Branch Details

* Main (Formerly Master) - Contains Tagged production ready code
* Develop - Contains developmental features and bug fixes not ready to be merged to a release branch
* Release - Contains production code for a specific release & associated bug fixes
* Hotfix - Priority production bug fixes
* Feature Branch - Contains developmental features and bug fixes that are still a work in progress



![Git flow](https://gblobscdn.gitbook.com/assets%2F-M15KrJzoMvhbv4NcO9o%2F-M4D_zaea7Lgc9yTKd8L%2F-M4Da-C19U9kv9CRce8Z%2Fgithub-flow.png?alt=media)



## Commits

Commits are the core of all development flow and are the key to maintaining readability within the flow. Messages should follow the below 7 rules to ensure commits contain all required information & maintain a clean history log;

**Required Read: ** https://chris.beams.io/posts/git-commit

1. [Separate subject from body with a blank line](https://chris.beams.io/posts/git-commit/#separate)
2. [Limit the subject line to 50 characters](https://chris.beams.io/posts/git-commit/#limit-50)
3. [Capitalize the subject line](https://chris.beams.io/posts/git-commit/#capitalize)
4. [Do not end the subject line with a period](https://chris.beams.io/posts/git-commit/#end)
5. [Use the imperative mood in the subject line](https://chris.beams.io/posts/git-commit/#imperative)
6. [Wrap the body at 72 characters](https://chris.beams.io/posts/git-commit/#wrap-72)
7. [Use the body to explain *what* and *why* vs. *how*](https://chris.beams.io/posts/git-commit/#why-not-how)



## Pull Requests

Pull requests should be made upon a feature or featureset has been completed. A completed feature must contain all relevant tests and should be subjected to passing CI prior to being merged.

The pull request must conform to the following

* Contain details of correctly referenced issues (Github/Fluxble)
* Contain a relevant title to the feature/set being merged
* Commits should be squashed unless the merge is part of a wider feature branch
* At least 1 other approver should validate the pull requests when merging to **Main**
* Regular code reviews should be undergone for pull requests to **Develop**



## Issues

To ensure the best resolution for an issue is reached, it is important that when logging issues developers should provide as much information as possible to speed up the investigation & debugging time of any issue, it should also contain clear reproduction steps and include any environmental/configuration information.

Developers should aim to provide prompt feedback for any issues they have logged and where nesessary raise any blocks/issues to their line managers when encountering delays. Issues should be proritised based on the amount of users/services affected or when assigned priority via a line manager.



### Creation

When creating issues. you should aim to include all of the following:

* Description of the issue in as much detail as possible
* Assigned to the relevant product owner/team
  * Where required, tag multiple teams within the issue body so all parties are aware
* Steps to reproduce the issue
  * When debugging HTTP endpoints a cURL request should be provided to replicate the issue
* User/Environmental information
  * User subject
  * Testing target
  * User role information
  * Device tokens
* Unit/Integration test illustrating the issue
* Logs showing any errors/information relating to the issue



## Tags & Versioning

Tags should be used to mark the completion of a feature/set, tags should follow the SemVar versioning schema and contain the `v` denotation as a prefix (example `v1.2.3`)

Upon a tag being set CI/CD will run against this tag to deploy to the relevent environments based on the branch it has been tagged against.


