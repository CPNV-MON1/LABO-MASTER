# Fork process

[Source](https://docs.github.com/en/get-started/quickstart/fork-a-repo)

<figure><img src="../../.gitbook/assets/image (4).png" alt=""><figcaption><p>Git-flow scenario to master</p></figcaption></figure>

* [ ] Fork the "upstream" repository in your github organisation

```
//TODO
![alt text](https://file.notion.so/f/s/7e3e07a9-e00b-4434-b41e-a7b6b23a967f/Untitled.png?id=a33c3042-eeac-406d-911d-0999b5a7e6bd&table=block&spaceId=1aaa7f1b-fcfb-4bd9-86c3-920f1f8b66fb&expirationTimestamp=1683712326001&signature=vp4i5MZ12430rrzueoWGU98SBsdCyoOHowaORoTM0Es&downloadName=Untitled.png "image Title")
```

* [ ] Clone your own repo in your local machine

```
[INPUT]
git clone https://github.com/andre1400/Labo-Master-1.git


[OUTPUT]
Cloning into 'Labo-Master-1'...
remote: Enumerating objects: 12, done.
remote: Counting objects: 100% (12/12), done.
remote: Compressing objects: 100% (11/11), done.
remote: Total 12 (delta 0), reused 12 (delta 0), pack-reused 0
Receiving objects: 100% (12/12), 4.28 KiB | 4.28 MiB/s, done.
```

* [ ] Init Git flow (with standard settings)

```
[INPUT]
git flow init -d

[OUTPUT]
Using default branch names.

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
Hooks and filters directory? [C:/Users/andre/Documents/cpnv/MON/Labo-Master-1/.git/hooks]
```

* [ ] Integrate updates from upstream (main) into your repository (develop)

```
[INPUT]
 git push --set-upstream origin develop

[OUTPUT]
Enumerating objects: 21, done.
Counting objects: 100% (21/21), done.
Delta compression using up to 8 threads
Compressing objects: 100% (20/20), done.
Writing objects: 100% (21/21), 6.26 KiB | 3.13 MiB/s, done.
Total 21 (delta 4), reused 10 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (4/4), done.
remote:
remote: Create a pull request for 'develop' on GitHub by visiting:
remote:      https://github.com/andre1400/Labo-Master-1/pull/new/develop
remote:
To https://github.com/andre1400/Labo-Master-1.git
 * [new branch]      develop -> develop
branch 'develop' set up to track 'origin/develop'
```

* [ ] Create a branch feature called "terraformBasicScript"

```
[INPUT]
git checkout -b terraformBasicScript

[OUTPUT]
Switched to a new branch 'terraformBasicScript'
```

* [ ] Add this code and commit it (feat:add basic terraform script")

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
[INPUT][OUTPUT]
PS C:\Users\andre\Documents\cpnv\MON\Labo-Master-1> git add .
PS C:\Users\andre\Documents\cpnv\MON\Labo-Master-1> git status
On branch terraformBasicScript
Your branch is up to date with 'origin/terraformBasicScript'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   terra.tf

PS C:\Users\andre\Documents\cpnv\MON\Labo-Master-1> git commit -m "add basic terraform script"
[terraformBasicScript 13b1b8e] add basic terraform script
 1 file changed, 23 insertions(+)
 create mode 100644 terra.tf
```

* [ ] Finish the feature

```
[INPUT]

[OUTPUT]
```

* Push this modification on your repository

```
[INPUT]
//git push

[OUTPUT]
//Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 547 bytes | 547.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/andre1400/Labo-Master-1.git
   36ebd4b..13b1b8e  terraformBasicScript -> terraformBasicScript
```

* What happens to the feature/branch ?

```
//TODO
git status
On branch feature/terraformBasicScript
Your branch is up to date with 'origin/feature/terraformBasicScript'.

nothing to commit, working tree clean
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
