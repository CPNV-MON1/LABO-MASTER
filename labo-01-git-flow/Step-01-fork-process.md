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
//TODO

[OUTPUT]
//TODO
```

* [ ] Finish the feature

```
[INPUT]
//TODO

[OUTPUT]
//TODO
```

* Push this modification on your repository

```
[INPUT]
//TODO

[OUTPUT]
//TODO
```

* What happens to the feature/branch ?

```
//TODO
Add your answer with command line used to validate your analysis.
```

* Open a pull request comparing your develop branch to your main
* Assign the pull request to your partner

```
//TODO
Screenshot pull request on github
```

* Notify him using a issue "Could you please review my pull request ?"

```
//TODO
Screenshot issue on github
```
