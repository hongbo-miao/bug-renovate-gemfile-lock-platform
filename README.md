# bug-renovate-gemfile-lock-platform

## Introduction

### Observed behavior

Renovate added `x86_64-linux` in **mobile-ios/Gemfile.lock** during lock file maintenance at https://github.com/Hongbo-Miao/bug-renovate-gemfile-lock-platform/pull/2

### Expected behavior

It should not add `x86_64-linux` in **mobile-ios/Gemfile.lock**, because the repo only works in `arm64-darwin-22` and `x86_64-darwin-19`.

## Ticket

Opened the ticket at https://github.com/renovatebot/renovate/issues/19134

## Renovate Log

<details>
  <summary>Click to expand</summary>

  ```shell
DEBUG: No dangling containers to remove
INFO: Repository started
{
  "renovateVersion": "34.37.0"
}
DEBUG: Using localDir: /mnt/renovate/gh/Hongbo-Miao/bug-renovate-gemfile-lock-platform
DEBUG: PackageFiles.clear() - Package files deleted
DEBUG: initRepo("Hongbo-Miao/bug-renovate-gemfile-lock-platform")
DEBUG: Using queue: host=api.github.com, concurrency=10
DEBUG: Hongbo-Miao/bug-renovate-gemfile-lock-platform default branch = main
DEBUG: Using app token for git init
DEBUG: Repository cache is restored from revision 13
DEBUG: Resetting npmrc
DEBUG: detectSemanticCommits()
DEBUG: checkOnboarding()
DEBUG: isOnboarded()
DEBUG: Checking cached config file name
DEBUG: GET https://api.github.com/repos/Hongbo-Miao/bug-renovate-gemfile-lock-platform/contents/renovate.json = (code=ERR_NON_2XX_3XX_RESPONSE, statusCode=404 retryCount=0, duration=183)
DEBUG: Existing config file no longer exists
DEBUG: findFile(renovate.json)
DEBUG: Initializing git repository into /mnt/renovate/gh/Hongbo-Miao/bug-renovate-gemfile-lock-platform
DEBUG: Performing blobless clone
DEBUG: git clone completed
{
  "durationMs": 946
}
DEBUG: latest repository commit
{
  "latestCommit": {
    "hash": "363c49eb69cb2372496ce83ce61ab869eda5ab38",
    "date": "2022-11-27T18:23:27-08:00",
    "message": "init",
    "refs": "HEAD -> main, origin/main, origin/HEAD",
    "body": "",
    "author_name": "Hongbo Miao",
    "author_email": "Hongbo.Miao@outlook.com"
  }
}
DEBUG: findFile(renovate.json5)
DEBUG: Config file exists, fileName: renovate.json5
DEBUG: Retrieving issueList
DEBUG: Retrieved 0 issues
DEBUG: Repo is onboarded
DEBUG: Found renovate.json5 config file
DEBUG: Repository config
{
  "fileName": "renovate.json5",
  "config": {
    "extends": [
      "config:base"
    ],
    "lockFileMaintenance": {
      "enabled": true
    }
  }
}
DEBUG: migrateAndValidate()
DEBUG: No config migration necessary
DEBUG: massaged config
{
  "config": {
    "extends": [
      "github>whitesource/merge-confidence:beta",
      "config:base"
    ],
    "lockFileMaintenance": {
      "enabled": true
    }
  }
}
DEBUG: migrated config
{
  "config": {
    "extends": [
      "github>whitesource/merge-confidence:beta",
      "config:base"
    ],
    "lockFileMaintenance": {
      "enabled": true
    }
  }
}
DEBUG: Setting hostRules from config
DEBUG: Found repo ignorePaths
{
  "ignorePaths": [
    "**/node_modules/**",
    "**/bower_components/**",
    "**/vendor/**",
    "**/examples/**",
    "**/__tests__/**",
    "**/test/**",
    "**/tests/**",
    "**/__fixtures__/**"
  ]
}
DEBUG: Using queue: host=api.github.com, concurrency=10
DEBUG: No vulnerability alerts found
DEBUG: No vulnerability alerts found
DEBUG: findIssue(Dependency Dashboard)
DEBUG: No baseBranches
DEBUG: extract()
DEBUG: Setting current branch to main
DEBUG: latest commit
{
  "branchName": "main",
  "latestCommitDate": "2022-11-27T18:23:27-08:00"
}
DEBUG: Using file match: (^|/)tasks/[^/]+\.ya?ml$ for manager ansible
DEBUG: Using file match: (^|/)requirements\.ya?ml$ for manager ansible-galaxy
DEBUG: Using file match: (^|/)galaxy\.ya?ml$ for manager ansible-galaxy
DEBUG: Using file match: (^|/)\.tool-versions$ for manager asdf
DEBUG: Using file match: azure.*pipelines?.*\.ya?ml$ for manager azure-pipelines
DEBUG: Using file match: (^|/)batect(-bundle)?\.yml$ for manager batect
DEBUG: Using file match: (^|/)batect$ for manager batect-wrapper
DEBUG: Using file match: (^|/)WORKSPACE(|\.bazel)$ for manager bazel
DEBUG: Using file match: \.bzl$ for manager bazel
DEBUG: Using file match: (^|\/)\.bazelversion$ for manager bazelisk
DEBUG: Using file match: (^|/)\.?bitbucket-pipelines\.ya?ml$ for manager bitbucket-pipelines
DEBUG: Using file match: buildkite\.ya?ml for manager buildkite
DEBUG: Using file match: \.buildkite/.+\.ya?ml$ for manager buildkite
DEBUG: Using file match: (^|/)Gemfile$ for manager bundler
DEBUG: Using file match: \.cake$ for manager cake
DEBUG: Using file match: (^|/)Cargo\.toml$ for manager cargo
DEBUG: Using file match: (^|/)\.circleci/config\.yml$ for manager circleci
DEBUG: Using file match: (^|/)cloudbuild\.ya?ml for manager cloudbuild
DEBUG: Using file match: (^|/)Podfile$ for manager cocoapods
DEBUG: Using file match: (^|/)([\w-]*)composer\.json$ for manager composer
DEBUG: Using file match: (^|/)conanfile\.(txt|py)$ for manager conan
DEBUG: Using file match: (^|/)(?:deps|bb)\.edn$ for manager deps-edn
DEBUG: Using file match: (^|/)(?:docker-)?compose[^/]*\.ya?ml$ for manager docker-compose
DEBUG: Using file match: (^|/|\.)Dockerfile$ for manager dockerfile
DEBUG: Using file match: (^|/)Dockerfile[^/]*$ for manager dockerfile
DEBUG: Using file match: (^|/)\.drone\.yml$ for manager droneci
DEBUG: Using file match: (^|/)fleet\.ya?ml for manager fleet
DEBUG: Using file match: (^|\/)flux-system\/(?:.+\/)?gotk-components\.yaml$ for manager flux
DEBUG: Using file match: (^|\/)\.fvm\/fvm_config\.json$ for manager fvm
DEBUG: Using file match: (^|/)\.gitmodules$ for manager git-submodules
DEBUG: Using file match: ^(workflow-templates|\.github\/workflows)\/[^/]+\.ya?ml$ for manager github-actions
DEBUG: Using file match: (^|\/)action\.ya?ml$ for manager github-actions
DEBUG: Using file match: \.gitlab-ci\.yml$ for manager gitlabci
DEBUG: Using file match: \.gitlab-ci\.yml$ for manager gitlabci-include
DEBUG: Using file match: (^|/)go\.mod$ for manager gomod
DEBUG: Using file match: \.gradle(\.kts)?$ for manager gradle
DEBUG: Using file match: (^|\/)gradle\.properties$ for manager gradle
DEBUG: Using file match: (^|\/)gradle\/.+\.toml$ for manager gradle
DEBUG: Using file match: \.versions\.toml$ for manager gradle
DEBUG: Using file match: (^|/)gradle/wrapper/gradle-wrapper\.properties$ for manager gradle-wrapper
DEBUG: Using file match: (^|/)requirements\.yaml$ for manager helm-requirements
DEBUG: Using file match: (^|/)values\.yaml$ for manager helm-values
DEBUG: Using file match: (^|/)helmfile\.yaml$ for manager helmfile
DEBUG: Using file match: (^|/)Chart\.yaml$ for manager helmv3
DEBUG: Using file match: (^|/)bin/hermit$ for manager hermit
DEBUG: Using file match: ^Formula/[^/]+[.]rb$ for manager homebrew
DEBUG: Using file match: \.html?$ for manager html
DEBUG: Using file match: (^|/)plugins\.(txt|ya?ml)$ for manager jenkins
DEBUG: Using file match: (^|/)jsonnetfile\.json$ for manager jsonnet-bundler
DEBUG: Using file match: ^.+\.main\.kts$ for manager kotlin-script
DEBUG: Using file match: (^|/)kustomization\.ya?ml$ for manager kustomize
DEBUG: Using file match: (^|/)project\.clj$ for manager leiningen
DEBUG: Using file match: (^|/|\.)pom\.xml$ for manager maven
DEBUG: Using file match: ^(((\.mvn)|(\.m2))/)?settings\.xml$ for manager maven
DEBUG: Using file match: (^|/)package\.js$ for manager meteor
DEBUG: Using file match: (^|\/)Mintfile$ for manager mint
DEBUG: Using file match: (^|/)mix\.exs$ for manager mix
DEBUG: Using file match: (^|\/)flake\.nix$ for manager nix
DEBUG: Using file match: (^|/)\.node-version$ for manager nodenv
DEBUG: Using file match: (^|/)package\.json$ for manager npm
DEBUG: Using file match: \.(?:cs|fs|vb)proj$ for manager nuget
DEBUG: Using file match: \.(?:props|targets)$ for manager nuget
DEBUG: Using file match: (^|\/)dotnet-tools\.json$ for manager nuget
DEBUG: Using file match: (^|\/)global\.json$ for manager nuget
DEBUG: Using file match: (^|/)\.nvmrc$ for manager nvm
DEBUG: Using file match: (^|/)([\w-]*)requirements\.(txt|pip)$ for manager pip_requirements
DEBUG: Using file match: (^|/)setup\.py$ for manager pip_setup
DEBUG: Using file match: (^|/)Pipfile$ for manager pipenv
DEBUG: Using file match: (^|/)pyproject\.toml$ for manager poetry
DEBUG: Using file match: (^|/)\.pre-commit-config\.yaml$ for manager pre-commit
DEBUG: Using file match: (^|/)pubspec\.ya?ml$ for manager pub
DEBUG: Using file match: (^|\/)Puppetfile$ for manager puppet
DEBUG: Using file match: (^|/)\.python-version$ for manager pyenv
DEBUG: Using file match: (^|/)\.ruby-version$ for manager ruby-version
DEBUG: Using file match: \.sbt$ for manager sbt
DEBUG: Using file match: project/[^/]*.scala$ for manager sbt
DEBUG: Using file match: (^|/)setup\.cfg$ for manager setup-cfg
DEBUG: Using file match: (^|/)Package\.swift for manager swift
DEBUG: Using file match: \.tf$ for manager terraform
DEBUG: Using file match: (^|/)\.terraform-version$ for manager terraform-version
DEBUG: Using file match: (^|/)terragrunt\.hcl$ for manager terragrunt
DEBUG: Using file match: (^|/)\.terragrunt-version$ for manager terragrunt-version
DEBUG: Using file match: \.tflint\.hcl$ for manager tflint-plugin
DEBUG: Using file match: ^\.travis\.yml$ for manager travis
DEBUG: Using file match: (^|/)\.vela\.ya?ml$ for manager velaci
DEBUG: Using file match: (^|\/)\.woodpecker[^/]*\.ya?ml$ for manager woodpecker
DEBUG: Matched 1 file(s) for manager bundler: mobile-ios/Gemfile
DEBUG: Matched 1 file(s) for manager ruby-version: mobile-ios/.ruby-version
DEBUG: Found Gemfile.lock file packageFile: mobile-ios/Gemfile
DEBUG: Found bundler package files
DEBUG: Found ruby-version package files
DEBUG: Found 2 package file(s)
INFO: Dependency extraction complete
{
  "baseBranch": "main",
  "stats": {
    "managers": {
      "bundler": {
        "fileCount": 1,
        "depCount": 2
      },
      "ruby-version": {
        "fileCount": 1,
        "depCount": 1
      }
    },
    "total": {
      "fileCount": 2,
      "depCount": 3
    }
  }
}
DEBUG: PackageFiles.add() - Package file saved for base branch
{
  "baseBranch": "main"
}
DEBUG: Package releases lookups complete
{
  "baseBranch": "main"
}
DEBUG: branchifyUpgrades
DEBUG: 1 flattened updates found:
DEBUG: Returning 1 branch(es)
DEBUG: config.repoIsOnboarded=true
DEBUG: packageFiles with updates
{
  "baseBranch": "main",
  "config": {
    "bundler": [
      {
        "packageFile": "mobile-ios/Gemfile",
        "registryUrls": [
          "https://rubygems.org"
        ],
        "deps": [
          {
            "depName": "ruby",
            "currentValue": "3.1.3",
            "datasource": "ruby-version",
            "registryUrls": null,
            "depIndex": 0,
            "updates": [],
            "warnings": [],
            "versioning": "ruby",
            "sourceUrl": "https://github.com/ruby/ruby",
            "homepage": "https://www.ruby-lang.org",
            "currentVersion": "3.1.3",
            "fixedVersion": "3.1.3"
          },
          {
            "depName": "slather",
            "managerData": {
              "lineNumber": 6
            },
            "currentValue": "'2.7.3'",
            "datasource": "rubygems",
            "lockedVersion": "2.7.3",
            "depIndex": 1,
            "updates": [],
            "warnings": [],
            "versioning": "ruby",
            "currentVersion": "2.7.3",
            "fixedVersion": "2.7.3"
          }
        ],
        "lockFiles": [
          "mobile-ios/Gemfile.lock"
        ]
      }
    ],
    "ruby-version": [
      {
        "packageFile": "mobile-ios/.ruby-version",
        "deps": [
          {
            "depName": "ruby",
            "currentValue": "3.1.3",
            "datasource": "ruby-version",
            "depIndex": 0,
            "updates": [],
            "warnings": [],
            "versioning": "ruby",
            "sourceUrl": "https://github.com/ruby/ruby",
            "homepage": "https://www.ruby-lang.org",
            "currentVersion": "3.1.3",
            "fixedVersion": "3.1.3"
          }
        ]
      }
    ]
  }
}
DEBUG: processRepo()
DEBUG: Processing 1 branch: renovate/lock-file-maintenance
DEBUG: Calculating hourly PRs remaining
DEBUG: getPrList success
{
  "pullsTotal": 1,
  "requestsTotal": 1,
  "apiQuotaAffected": true
}
DEBUG: currentHourStart=2022-11-28T02:00:00.000+00:00
DEBUG: PR hourly limit remaining: 2
DEBUG: Calculating prConcurrentLimit (10)
DEBUG: getBranchPr(renovate/lock-file-maintenance)
DEBUG: findPr(renovate/lock-file-maintenance, undefined, open)
DEBUG: findPr(renovate/lock-file-maintenance, undefined, closed)
DEBUG: 0 PRs are currently open
DEBUG: PR concurrent limit remaining: 10
DEBUG: Calculated maximum PRs remaining this run: 2
DEBUG: PullRequests limit = 2
DEBUG: Calculating hourly PRs remaining
DEBUG: currentHourStart=2022-11-28T02:00:00.000+00:00
DEBUG: PR hourly limit remaining: 2
DEBUG: Calculating branchConcurrentLimit (10)
DEBUG: 0 already existing branches found:
DEBUG: Branch concurrent limit remaining: 10
DEBUG: Calculated maximum branches remaining this run: 2
DEBUG: Branches limit = 2
DEBUG: syncBranchState()(branch="renovate/lock-file-maintenance")
DEBUG: syncBranchState(): Branch cache not found, creating minimal branchState(branch="renovate/lock-file-maintenance")
DEBUG: getBranchPr(renovate/lock-file-maintenance)(branch="renovate/lock-file-maintenance")
DEBUG: findPr(renovate/lock-file-maintenance, undefined, open)(branch="renovate/lock-file-maintenance")
DEBUG: findPr(renovate/lock-file-maintenance, undefined, closed)(branch="renovate/lock-file-maintenance")
DEBUG: branchExists=false(branch="renovate/lock-file-maintenance")
DEBUG: dependencyDashboardCheck=undefined(branch="renovate/lock-file-maintenance")
DEBUG: recreateClosed is true(branch="renovate/lock-file-maintenance")
DEBUG: Checking schedule(before 5am on monday, null)(branch="renovate/lock-file-maintenance")
DEBUG: Checking 1 schedule(s)(branch="renovate/lock-file-maintenance")
DEBUG: Checking schedule "before 5am on monday"(branch="renovate/lock-file-maintenance")
{
  "parsedSchedule": {
    "schedules": [
      {
        "t_b": [
          18000
        ],
        "d": [
          2
        ]
      }
    ],
    "exceptions": [],
    "error": -1
  }
}
DEBUG: Matches schedule before 5am on monday(branch="renovate/lock-file-maintenance")
DEBUG: Branch needs creating(branch="renovate/lock-file-maintenance")
DEBUG: Using reuseExistingBranch: false(branch="renovate/lock-file-maintenance")
DEBUG: Setting current branch to main(branch="renovate/lock-file-maintenance")
DEBUG: latest commit(branch="renovate/lock-file-maintenance")
{
  "branchName": "main",
  "latestCommitDate": "2022-11-27T18:23:27-08:00"
}
DEBUG: manager.getUpdatedPackageFiles() reuseExistingBranch=false(branch="renovate/lock-file-maintenance")
DEBUG: bundler.updateArtifacts(mobile-ios/Gemfile)(branch="renovate/lock-file-maintenance")
DEBUG: Using bundler version specified in lockfile(branch="renovate/lock-file-maintenance")
DEBUG: Using ruby version from gemfile(branch="renovate/lock-file-maintenance")
DEBUG: Setting CONTAINERBASE_CACHE_DIR to /tmp/containerbase(branch="renovate/lock-file-maintenance")
DEBUG: Using docker to execute(branch="renovate/lock-file-maintenance")
{
  "image": "ruby"
}
DEBUG: containerbaseDir is separate from cacheDir(branch="renovate/lock-file-maintenance")
DEBUG: Found version constraint - checking for a compatible image to use(branch="renovate/lock-file-maintenance")
{
  "depName": "docker.io/renovate/ruby",
  "scheme": "ruby",
  "constraint": "3.1.3"
}
DEBUG: Found compatible image version(branch="renovate/lock-file-maintenance")
{
  "depName": "docker.io/renovate/ruby",
  "scheme": "ruby",
  "constraint": "3.1.3",
  "version": "3.1.3"
}
DEBUG: Resolved tag constraint(branch="renovate/lock-file-maintenance")
{
  "image": "docker.io/renovate/ruby",
  "tagConstraint": "3.1.3",
  "tagVersioning": "ruby",
  "tag": "3.1.3"
}
DEBUG: Fetching Docker image: docker.io/renovate/ruby:3.1.3(branch="renovate/lock-file-maintenance")
DEBUG: Finished fetching Docker image docker.io/renovate/ruby:3.1.3@sha256:b7a5e415baf4f9ee62ab9757437ce4dc974ed4a382e13bffc1f3f20364360d96(branch="renovate/lock-file-maintenance")
DEBUG: Executing command(branch="renovate/lock-file-maintenance")
{
  "command": "docker run --rm --name=renovate_ruby --label=renovate_child -v \"/mnt/renovate/gh/Hongbo-Miao/bug-renovate-gemfile-lock-platform\":\"/mnt/renovate/gh/Hongbo-Miao/bug-renovate-gemfile-lock-platform\" -v \"/tmp/renovate-cache\":\"/tmp/renovate-cache\" -v \"/tmp/containerbase\":\"/tmp/containerbase\" -e BUNDLE_GITHUB__COM -e GEM_HOME -e BUILDPACK_CACHE_DIR -e CONTAINERBASE_CACHE_DIR -w \"/mnt/renovate/gh/Hongbo-Miao/bug-renovate-gemfile-lock-platform/mobile-ios\" docker.io/renovate/ruby:3.1.3 bash -l -c \"install-tool bundler 2.3.26 && ruby --version && bundler lock --update\""
}
DEBUG: exec completed(branch="renovate/lock-file-maintenance")
{
  "durationMs": 9017,
  "stdout": "Installing v1 tool bundler v2.3.26\nSuccessfully installed bundler-2.3.26\n1 gem installed\nBundler version 2.3.26\nInstalled v1 bundler in 2 seconds\nskip cleanup, not a docker build: 087d58923bc4\nruby 3.1.3p185 (2022-11-24 revision 1a6b16756e) [x86_64-linux]\nFetching gem metadata from https://rubygems.org/........\nResolving dependencies...\nWriting lockfile to /mnt/renovate/gh/Hongbo-Miao/bug-renovate-gemfile-lock-platform/mobile-ios/Gemfile.lock\n",
  "stderr": ""
}
DEBUG: Returning updated Gemfile.lock(branch="renovate/lock-file-maintenance")
DEBUG: No package files need updating(branch="renovate/lock-file-maintenance")
DEBUG: Updated 1 lock files(branch="renovate/lock-file-maintenance")
{
  "updatedArtifacts": [
    "mobile-ios/Gemfile.lock"
  ]
}
DEBUG: 1 file(s) to commit(branch="renovate/lock-file-maintenance")
DEBUG: Preparing files for committing to branch renovate/lock-file-maintenance(branch="renovate/lock-file-maintenance")
DEBUG: Setting git author name: Renovate Bot(branch="renovate/lock-file-maintenance")
DEBUG: Setting git author email: bot@renovateapp.com(branch="renovate/lock-file-maintenance")
DEBUG: git commit(branch="renovate/lock-file-maintenance")
{
  "deletedFiles": [],
  "ignoredFiles": [],
  "result": {
    "author": null,
    "branch": "renovate/lock-file-maintenance",
    "commit": "c23bda9165b14af07a80028cf888bb2b0b90ca4a",
    "root": false,
    "summary": {
      "changes": 1,
      "insertions": 3,
      "deletions": 0
    }
  }
}
DEBUG: resetToCommit(363c49eb69cb2372496ce83ce61ab869eda5ab38)(branch="renovate/lock-file-maintenance")
DEBUG: Fetching branch renovate/lock-file-maintenance(branch="renovate/lock-file-maintenance")
INFO: Branch created(branch="renovate/lock-file-maintenance")
{
  "commitSha": "f29a9da4fe6df5ebf3965cd56ad112c4cfd326ad"
}
DEBUG: Ensuring PR(branch="renovate/lock-file-maintenance")
DEBUG: There are 0 errors and 0 warnings(branch="renovate/lock-file-maintenance")
DEBUG: getBranchPr(renovate/lock-file-maintenance)(branch="renovate/lock-file-maintenance")
DEBUG: findPr(renovate/lock-file-maintenance, undefined, open)(branch="renovate/lock-file-maintenance")
DEBUG: findPr(renovate/lock-file-maintenance, undefined, closed)(branch="renovate/lock-file-maintenance")
DEBUG: Creating PR(branch="renovate/lock-file-maintenance")
{
  "prTitle": "Lock file maintenance"
}
DEBUG: Creating PR(branch="renovate/lock-file-maintenance")
{
  "title": "Lock file maintenance",
  "head": "Hongbo-Miao:renovate/lock-file-maintenance",
  "base": "main",
  "draft": false
}
DEBUG: PR created(branch="renovate/lock-file-maintenance")
{
  "pr": 2,
  "draft": false
}
DEBUG: Adding labels '' to #2(branch="renovate/lock-file-maintenance")
INFO: PR created(branch="renovate/lock-file-maintenance")
{
  "pr": 2,
  "prTitle": "Lock file maintenance"
}
DEBUG: addParticipants(pr=2)(branch="renovate/lock-file-maintenance")
DEBUG: Created Pull Request #2(branch="renovate/lock-file-maintenance")
DEBUG: PR is not configured for automerge(branch="renovate/lock-file-maintenance")
DEBUG: setBranchCommit()(branch="renovate/lock-file-maintenance")
DEBUG: getBranchPr(renovate/lock-file-maintenance)
DEBUG: findPr(renovate/lock-file-maintenance, undefined, open)
DEBUG: Found PR #2
DEBUG: branch.isBehindBase(): using cached result "false"
DEBUG: isBranchConflicted(main, renovate/lock-file-maintenance)
DEBUG: branch.isConflicted(): using cached result "false"
DEBUG: Ensuring Dependency Dashboard
DEBUG: ensureIssue(Dependency Dashboard)
INFO: Issue created
DEBUG: Removing any stale branches
DEBUG: config.repoIsOnboarded=true
DEBUG: Branch lists
{
  "branchList": [
    "renovate/lock-file-maintenance"
  ],
  "renovateBranches": [
    "renovate/configure",
    "renovate/lock-file-maintenance"
  ]
}
DEBUG: remainingBranches=renovate/configure
DEBUG: findPr(renovate/configure, undefined, open)
DEBUG: branch.isModified(): using git to calculate
DEBUG: branch.isModified() = false
DEBUG: setCachedModifiedResult(): Branch cache not present
INFO: Deleting orphan branch(branch="renovate/configure")
DEBUG: Git function thrown
{
  "err": {
    "task": {
      "commands": [
        "push",
        "--delete",
        "origin",
        "renovate/configure"
      ],
      "format": "utf-8",
      "parser": "[function]"
    },
    "message": "error: unable to delete 'renovate/configure': remote ref does not exist\nerror: failed to push some refs to 'https://github.com/Hongbo-Miao/bug-renovate-gemfile-lock-platform.git'\n",
    "stack": "Error: error: unable to delete 'renovate/configure': remote ref does not exist\nerror: failed to push some refs to 'https://github.com/Hongbo-Miao/bug-renovate-gemfile-lock-platform.git'\n\n    at Object.action (/home/ubuntu/renovateapp/node_modules/simple-git/dist/cjs/index.js:1261:25)\n    at PluginStore.exec (/home/ubuntu/renovateapp/node_modules/simple-git/dist/cjs/index.js:1296:29)\n    at /home/ubuntu/renovateapp/node_modules/simple-git/dist/cjs/index.js:1661:43\n    at new Promise (<anonymous>)\n    at GitExecutorChain.handleTaskData (/home/ubuntu/renovateapp/node_modules/simple-git/dist/cjs/index.js:1659:16)\n    at GitExecutorChain.<anonymous> (/home/ubuntu/renovateapp/node_modules/simple-git/dist/cjs/index.js:1643:44)\n    at Generator.next (<anonymous>)\n    at fulfilled (/home/ubuntu/renovateapp/node_modules/simple-git/dist/cjs/index.js:55:24)\n    at runMicrotasks (<anonymous>)\n    at processTicksAndRejections (node:internal/process/task_queues:96:5)"
  }
}
DEBUG: No remote branch to delete with name: renovate/configure
DEBUG: No local branch to delete with name: renovate/configure
DEBUG: Retrieving issueList
DEBUG: Retrieved 1 issues
DEBUG: Cleaning up Renovate refs: refs/renovate/*
DEBUG: PackageFiles.clear() - Package files deleted
DEBUG: Branch summary
{
  "cacheModified": true,
  "baseBranches": [
    {
      "branchName": "main",
      "sha": "363c49eb69cb2372496ce83ce61ab869eda5ab38"
    }
  ],
  "branches": [
    {
      "branchName": "renovate/lock-file-maintenance",
      "branchSha": "f29a9da4fe6df5ebf3965cd56ad112c4cfd326ad",
      "baseBranch": "main",
      "baseBranchSha": "363c49eb69cb2372496ce83ce61ab869eda5ab38",
      "automerge": false,
      "isModified": false
    }
  ],
  "inactiveBranches": []
}
DEBUG: Renovate repository PR statistics
{
  "stats": {
    "total": 1,
    "open": 1,
    "closed": 0,
    "merged": 0
  }
}
DEBUG: Repository result: done, status: onboarded, enabled: true, onboarded: true
DEBUG: Repository timing splits (milliseconds)
{
  "splits": {
    "init": 4762,
    "extract": 1262,
    "lookup": 1177,
    "onboarding": 0,
    "update": 40675
  },
  "total": 50813
}
DEBUG: Package cache statistics
{
  "get": {
    "count": 4,
    "avgMs": 48,
    "medianMs": 10,
    "maxMs": 153
  },
  "set": {
    "count": 0
  }
}
DEBUG: http statistics
{
  "urls": {
    "https://api.github.com/graphql (POST,200)": 3,
    "https://api.github.com/repos/Hongbo-Miao/bug-renovate-gemfile-lock-platform/contents/renovate.json (GET,404)": 1,
    "https://api.github.com/repos/Hongbo-Miao/bug-renovate-gemfile-lock-platform/git/commits (POST,201)": 1,
    "https://api.github.com/repos/Hongbo-Miao/bug-renovate-gemfile-lock-platform/git/refs (POST,201)": 1,
    "https://api.github.com/repos/Hongbo-Miao/bug-renovate-gemfile-lock-platform/git/trees (POST,201)": 1,
    "https://api.github.com/repos/Hongbo-Miao/bug-renovate-gemfile-lock-platform/issues (POST,201)": 1,
    "https://api.github.com/repos/Hongbo-Miao/bug-renovate-gemfile-lock-platform/pulls (GET,200)": 1,
    "https://api.github.com/repos/Hongbo-Miao/bug-renovate-gemfile-lock-platform/pulls (POST,201)": 1,
    "https://api.github.com/repos/whitesource/merge-confidence/contents/beta.json (GET,200)": 1
  },
  "hostStats": {
    "api.github.com": {
      "requestCount": 11,
      "requestAvgMs": 342,
      "queueAvgMs": 0
    }
  },
  "totalRequests": 11
}
DEBUG: dns cache
{
  "hosts": [
    "api.github.com"
  ]
}
INFO: Repository finished
{
  "cloned": true,
  "durationMs": 50813
}
  ```
</details>
