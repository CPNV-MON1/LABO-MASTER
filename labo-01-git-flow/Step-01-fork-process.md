# Fork process

[Source](https://docs.github.com/en/get-started/quickstart/fork-a-repo)

<figure><img src="../../.gitbook/assets/image (4).png" alt=""><figcaption><p>Git-flow scenario to master</p></figcaption></figure>

* [ ] Fork the "upstream" repository in your github organisation

```
//TODO
Screenshot of Github
```

* [ ] Clone "teacher" repo in your local machine

```
[INPUT]
git clone https://github.com/DylanBerney/MON-Labo-Master.git

[OUTPUT]
Cloning into 'MON-Labo-Master'...
remote: Enumerating objects: 12, done.
remote: Counting objects: 100% (12/12), done.
remote: Compressing objects: 100% (11/11), done.
remote: Total 12 (delta 0), reused 12 (delta 0), pack-reused 0
Receiving objects: 100% (12/12), 4.28 KiB | 4.28 MiB/s, done.

```

* [ ] Init Git flow (with standard settings)

```
[INPUT]
git flow init

[OUTPUT]
Which branch should be used for bringing forth production releases?
   - main
Branch name for production releases: [main]
Branch name for "next release" development: [develop]

How to name your supporting branch prefixes?
Feature branches? [feature/]
Bugfix branches? [bugfix/]
Release branches? [release/]
Hotfix branches? [hotfix/]
Support branches? [support/]
Version tag prefix? []
Hooks and filters directory? [C:/Users/Dylan/MON-Labo-Master/.git/hooks]
```

* [ ] Update your develop branch directly to the upstream (main branch)

```
[INPUT]
git push --set-upstream origin develop

[OUTPUT]
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
remote:
remote: Create a pull request for 'develop' on GitHub by visiting:
remote:      https://github.com/DylanBerney/MON-Labo-Master/pull/new/develop
remote:
To https://github.com/DylanBerney/MON-Labo-Master.git
 * [new branch]      develop -> develop
branch 'develop' set up to track 'origin/develop'.
```

* [ ] Create a branch feature called "feat:add terraform basic  script"

```
[INPUT]
git flow feature start terraform

[OUTPUT]
Switched to a new branch 'feature/terraform'
M       labo-01-git-flow/Step-01-fork-process.md

Summary of actions:
- A new branch 'feature/terraform' was created, based on 'develop'
- You are now on branch 'feature/terraform'

Now, start committing on your feature. When done, use:

     git flow feature finish terraform

```

* [ ] Add this code and commit it

```
terraform {
  required_providers {
    aws = {
      source  = "hashicorp/aws"
      version = "~> 4.16"
    }
  }

  required_version = ">= 1.2.0"
}

provider "aws" {
  region  = "us-west-2"
}

resource "aws_instance" "app_server" {
  ami           = "ami-830c94e3"
  instance_type = "t2.micro"

  tags = {
    Name = "ExampleAppServerInstance"
  }
}
```

```
[INPUT]
git add .

git commit -m "feat:add basic terraform script"

[OUTPUT]
[feature/terraform 524e962] feat:add basic terraform script
 2 files changed, 66 insertions(+), 8 deletions(-)
 create mode 100644 basic terraform script.py
```

* [ ] Finish the feature

```
[INPUT]
git flow feature finish terraform

[OUTPUT]
Merge made by the 'ort' strategy.
 basic terraform script.py                | 23 +++++++++++++
 labo-01-git-flow/Step-01-fork-process.md | 59 ++++++++++++++++++++++++++------
 2 files changed, 72 insertions(+), 10 deletions(-)
 create mode 100644 basic terraform script.py
Deleted branch feature/terraform (was 6d72425).

Summary of actions:
- The feature branch 'feature/terraform' was merged into 'develop'
- Feature branch 'feature/terraform' has been locally deleted
- You are now on branch 'develop'

```

* Push this modification on your repository

```
[INPUT]
$ git push --set-upstream origin develop

[OUTPUT]
Enumerating objects: 13, done.
Counting objects: 100% (13/13), done.
Delta compression using up to 4 threads
Compressing objects: 100% (10/10), done.
Writing objects: 100% (10/10), 2.58 KiB | 1.29 MiB/s, done.
Total 10 (delta 3), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (3/3), done.
To https://github.com/DylanBerney/MON-Labo-Master.git
   094d8ba..9b5fdc8  develop -> develop
branch 'develop' set up to track 'origin/develop'.
```

* What happens to the feature/branch ?

```
//TODO
Deleted branch feature/terraform (was 6d72425).
La branch c'est fait effacer durant le merge entre la feature et le developp
```

* Open a pull request comparing your develop branch to your main
* Assign the pull request to your partner

```
//TODO
Screenshot pull request on github
(C:\Users\Dylan\Pictures\Capture.PNG)

* Notify him using a issue "Could you please review my pull request ?"

```
//TODO
Screenshot issue on github
```
