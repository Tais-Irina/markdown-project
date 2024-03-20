# ��������� �� GIT  � GITHUB
---

## GIT 

GIT - ������� �������� ������

## ��������� ������

����������� ������������� Git ���������� ������� � �������� ������, ������� �� ��, ��� ��������� � macOS � Linux. 

��� ����� ����� ���������� ����������� ���������� ���������� ��� Windows, ������� ���������� Git Bash.

�� ��������� �� ������ Bash, �� � ��� Git


## ��������� GIT

### ������ � ������ ��������� **.gitconfig**
����� ������������ Git � ������� � ���������� ������� ���� �������, ��� � ����� ��������� ������, ����� ������������� � ������� ��� ������������ � ����� ����������� �����.

�� ����� ��������, � ����� ���������� �� ���������� ����� ������: ����� git config --global ��������� �����.


```BASH
$ git config --global user.name "User Namovich" 
# ��� ��� ��� ����� �������� ��������� � � ��������

$ git config --global user.email username@yandex.ru
# ����� ����� ������� ���� ��������� email 
```

��� ���������� ��������� Git ������ � ����� .gitconfig � �������� ����������. ������� ������� � ���� ���� ��������� ��� � �����. ����� ��������� � ����, ����� ������� ������� ��� ������ ������.

```
$ cat ~/.gitconfig 
```

������ ������ �������� � ������� ���������� ����� ������������ Git ��� �� �������� git config � ������ --list (����. �������).
```
$ git config --list 
```

## ������� ��������� �����������

### �������������� ����������� � **git init**

����� Git ����� ����������� ��������� � �������, ����� � ������� ����� ������� ����� ������� Git-������������. ��� ����� ������� ������������� � �� � ������ ������� git init
```
$ cd ~/dev/first-project # ������� � ������ �����
$ git init # ������� �����������
```
� �������� .git Git ����� ������� ��� ��������� ����������.

**����������� �����, ���� ���-�� ����� �� ���, � rm -rf .git**
```
$ cd <����� � ������������> # ������� � �����

$ rm -rf .git # ������� �������� .git
```
-rf:
* ���� -r (�� ����. recursive � �����������) ��������� ������� ����� ������ � �� ����������;
* ���� -f (�� ����. force � �����������) ������� ��� �� �������� ����� ��� ����� ������ ������� ���� ����? � ����? � ���� ����?�.

###��������� ��������� ����������� � **git status**

����� ������������� ����������� first-project ��������� ������� git status � ��� ���������� ������� ��������� �����������.

### ����������� ����� � ���������� � **git add**

�������� ����� todo.txt � readme.txt � ����� first-project 

�� ����� ����������� ��������� �����, ������� ����� ������������ ������� git add --all. 
```
$ touch todo.txt
$ touch readme.txt
# ������� ����� todo.txt � readme.txt

$ git add --all # ����������� � ���������� ��� ����� � �����������
$ git status # ��������� ������  
```

��������� ����� ����� � �� ������.
```
$ git add todo.txt
$ git add readme.txt
$ git status 
```

����� ����� �������� ������� ����� �������. ���������� � ������� ����� � Bash ��������� ����� (.).

```
$ git add . # �������� ��� ������� �����
$ git status 
```

### ������ ������ � **git commit**

������ �����������, ��� ��������� ����� ��������� � ������� � ��� ������������� � ��� ����� ����� ������������. 

g�������� � ����� first-project � ��������� ������ �� ��������� ������������.

```
$ git commit -m '��� ������ ������!' 
```

���� -m ����������� ������� ���������.
������ � ����� ��������� ����������, � ��� ������ �������� ���������. ��� ������� ����� ����� -m � ��������.


��������� ������� ������� ������ mermaid:
* flowchart TD ����-����� ���������
* graph LR - ������� ������������ �����

������������ ���� �����:

```mermaid
flowchart TD
A[Save file.txt in project dir] --> B[git add file.txt];
B --> D["git commit -m 'Comments about commit'"];
``` 

�������������� ���� �����:

```mermaid
graph LR
A[Save file.txt in project dir] --> B[git add file.txt] --> D["git commit -m 'Comments about commit'"];
``` 

### ������������� ������� �������� � **git log**

����� ������� ��� �������, ������� ������� git log.

�������� ��������, ��� �� ��������� git log ������� ������� � �������� ��������������� ������� � ��������� ������� ����������� ������� ������. � ���� ����� ���������, ���� ���������� �� ���� � ����� �� ��������.

## ������� ��������� ����������� �� **GitHub**

GitHub � ��������� ��� �������� IT-�������� � ���������� ������ ��� ���� � �������������� Git. �� ����, ��� ����, ���� ����� ��������� ����� ������ ������� ��� ������ � ������� ������.

Git � GitHub � ��� ��� ������ �������, ������� ����������� ���������� ���� �� �����. 

Git:
- ���������� ���������� ��� ������ � ���������� � ��������� �������������;
- ������ � �������� �������� �����.

GitHub:
- ��������� ��� ���������� �������� ������������;
- ����������� �������� Microsoft.

**����������**

1. ������� � ���� ������� �� ������ https://github.com/username, ��� username � ���, ������� �� ������� ��� �����������.
1. �������� �����������. ��� ����� ��������� �� ������� Repositories (����. ������������), � ����� ������� �� ������ ������ New (����. ������) ������.
1. ��������� ���� �������� ������ �����������. �������� ��� first-project. �������� ��������� ����������� ������������� ������ ��������� � ������ ����� ������� � ��� �� ����������. �� ����� �� ��������, ����� �������� �� ���������.

������ ���� ��� ���� �� �����������. ����� ��������� �� ������ ������ Create repository (����. �������� �����������) �����.

�������� ������� �������� ����������� � ���������, ������� ��� ���� �� ����� ����������.

�� ������, ����� ��������� ������ � GitHub � ������� � ����� ����������, �� ��������� ������������ SSH-����� (�� ����. Secure Shell � ����������� ��������).


## ������������� ������������

### ��������� SSH ������

**��� ����� SSH**

����� ���������� ������������ ������� � ����, ��� ������� ������� ���������� � �������� ������ ������� ����� ������������.

���� �� �������� ���������������� ������� ���������� � SSH (�� ����. Secure Shell Protocol).

�� ������������ ���������� ����� ������� � ����. � ������� ����� ��������� ����� �������� ������ � ��������� ���������� ��� ���������� �� �� ����. ������ ���������, ������� �������� ���������.

SSH ���������� ���� ������ ��� ����������� ������������ � ��������� � ���������: 
* ��������� ���� (����. private key) �������� ������ �� ����� ���������� � �� ������ ������������ ����-���� ���. �� ������������ ��� ����������� ������.
* ��������� ���� (����. public key) �������� ���� � ������������ ��� ���������� ������. ��� ����� ���� ������������ ������ ��������� ������.

������ �� ������ ������������ ������ � ������� ���������� �����, �� ����� �������� ���������� ����� ����� �� ��� ��� �����������. ��� ��� ����� ������� � �������� SSH-����.

� ������� �� ��������� ������ ������������ �� ��� �������������� � GitHub � ������� ��������� ���������.

**�������� ������� SSH-�����**

������ ��� ������������ SSH-�����, ���������, ��� � ��� �� ��� ���. �� ��������� ���������� � SSH-������� ��������� � �������� ���������� ������������. ��������� � ��.

������ SSH-����� ��������� � ���������� .ssh/. ��������� ������� ���� ���������� � ������ � ��� ����� � ������� ��������� �������.

```
$ cd ~ # ������� � �������� ���������� 
$ ls -la .ssh/ # ������ ������ ��������� ������ 
```

���� ����� ������ ��� � ���, �� � �������. 
���� ���� ����� � �������� ����������, SSH-����� ��� �����������:

* id_dsa.pub;
id_ecdsa.pub;
id_ed25519.pub;
id_rsa.pub.

���� �� �� ��������� ��� �����, ������� �� ���.

**���������� ��������� SSH ������**

1. ��� ��������� SSH-���� ����� ������������ ��������� ssh-keygen. �������� �������� � ������� ��������� �������.
```
$ ssh-keygen -t ed25519 -C "����������� �����, � ������� �������� ��� ������� �� GitHub" 
```

����������� ����������� �����, � ������� �������� ��� GitHub-�������.
    
���� �� ������ ��������� �� ������, ��, ������ �����, ���� ������� �� ������������ �������� ���������� ed25519. ������ ���������: ����������� ������ ��������.

```
$ ssh-keygen -t rsa -b 4096 -C "����������� �����, � ������� �������� ��� ������� �� GitHub" 
```

2. ������� ����� �������� ������. ������� ������� � ������� �������� ������� ������������ ���� �� ���������. ��� ����� ������� Enter.

3. ��������� �������� ������� ����� (����. passphrase) ��� ������� � SSH-�����. �� ������ �������� ���� ������. ��� ����� ������� Enter, � ����� ��� ��� Enter ��� �������������.

> Enter passphrase (empty for no passphrase): [Type a passphrase]
> Enter same passphrase again: [Type passphrase again] 

4. ������! ������ �������� ���������, ��� ����� ������������� ���������������. ��� ����� �������� ��� �������.

```BACH
ls -a ~/.ssh 
```

 �� ������ ������ ��������� ��� ����� � ���� � ����������� .pub, ������ � ���. ���� � .pub � ���������, �� ����� �������� � ���-������� ��� ���������. ���� ��� ���������� .pub � ���������. �� � ���� ������ �� ����������� ��� ������! 


### �������� SSH ����� � GitHub

1. ����� ���������� ������� `ssh-keygen` �� ����������� ����� � ���������� `~/.ssh` ����� ������� ��� ����� � `id_ed25519` � `id_ed25519.pub` (��� `id_rsa` � `id_rsa.pub` � � ����������� �� ����, ����� �������� �� ������������):
* `id_ed25519/id_rsa` � ��������� ���� (���� ��� .pub � �����). �� � ���� ������ �� ��������� ��� � �� �������� ��.
* `id_ed25519.pub/id_rsa.pub` � ��������� ���� (�� ��� ��������� ���������� .pub).
���������� ���������� ����� � ��������� ������ � ����� ������.

```
# ����������� ���������� ����� � ����� ������:
$ clip < ~/.ssh/id_rsa.pub
# ��� ed25519:
$ clip < ~/.ssh/id_ed25519.pub 
```

���� clip �� ���������, �������� ���������� ����� � ������� 

```
cat ~/.ssh/id_rsa.pub
# ��� 
cat ~/.ssh/id_ed25519.pub 

```
 � ���������� ����� � ����� ������ �� �������.

2. ��������� �� GitHub � �������� ����� Settings (����. ����������) � ���� ��������. 
3. � ���� ����� ������� �� ����� SSH and GPG keys.
4. � ����������� ������� �������� New SSH key (����. ������ SSH-�����).
5. � ���� Title (����. ����������) �������� �������� �����. ��������, Personal key (����. ������� �����).
6. � ���� Key type (����. ���� �����) ������ ���� Authentication Key (����. ����� ��������������).
7. � ���� Key ���������� ��� ���� �� ������ ������.
8. ������� �� ������ Add SSH key (����. ��������� SSH-�����).
9. ��������� ������������ ����� � ������� ��������� �������.

```BASH
$ ssh -T git@github.com 
```

10. ������� `yes`, ����� ����������. �� ������� ����������� �� ������.

### ���������� ���������� � ���������� ������������ � **git remote add**

��������� �� �������� ��������� �����������, �������� ��� SSH � ���������� URL. ������ ������ �������� ������� ��� ���������.

�������� �������, ��������� � ������� ���������� ����������� � ������� ������� `git remote add`

```BASH
$ cd ~/dev/first-project
$ git remote add origin git@github.com:%���_��������%/first-project.git 
```

������� ���������� �������� ��� ���������: ��� ��������� ����������� � ��� URL. � �������� ����� ����������� ����� origin. � URL �� ����������� �� �������� ��������� �����������.

`origin` (����. ���������) � ����������� ���������, � ������� �������� ����� ���������� � �������� ��������� ����������� (������ ����� ����������� ����). ��� ����������� �������� ������.

### ���������, ��� ����������� �������, **� git remote -v**

����� ���������, ��� ����������� �������, ���������:

```
$ git remote -v

origin    git@github.com:%���_��������%/%���-�������%.git (fetch)
origin    git@github.com:%���_��������%/%���-�������%.git (push) 
```

� ������ �� ������ ������� ��� �������, ����������� ���, ��� �������� ����.
���� -v � �������� ����� ����� --verbose (����. ����������). �� ��������� �������� ������ ���������� � ������.

### ��������� ��������� �� �������� ����������� � **git push**

� ������ ��� ��� ������� ����� ������� � ������ -u � ����������� origin (��� ��������� �����������) � main ��� master (�������� ������� �����). 

���� -u ������ ��������� ����� � ���������� ��������. ��� �� ��������� ��������� � �������� ����������� � ���������� �����, ��� �� � ����� ����� ������������� ������� �����.

```
$ git push -u origin main # ���� ������� ������� � ������, ���������� 
                          # �������� main �� master. 
```

� ���������� ��� ������ � �������� ������������ ���� -u ����� �������� � ������ ������:

```
git push
```

## ��� - ������������� �������

**�����������** (�� ����. hash, ��������, ���������, ���������) � ��� ������ ������������� ����� ������ � �������� �� ���������� (����. fingerprint).

���������� � ������� � ��� ����� ������: ����� ��� ������ ������, ���������� ������ � ����������� �� ������ ������� � ������ �� ����������, ��� ������������ (����. parent), ������.

Git �������� (�����������) ���������� � ������� � ������� ��������� SHA-1 (�� ����. Secure Hash Algorithm � ����������� �������� ������������) � �������� ��� ������� ������� ���� ���������� ��� � ��������� �����������.
������ ��� � ��� �������� (40 �������� � ������ SHA-1) ������, ������� ������� �� ���� � ��������� ���� A�F (�������, ��������� ��� ��������).

��� �������� ���������� ������� ����������:
* ���� ��� �������� ������ ��� ������ � ���� �� ������ ������� ������, �� ��������� ����� �������������� ����������;
* ���� ���� ���-�� � �������� ������ ���������� (���� �� ���� ������), �� ��� ���� ��������� (������ ������).

����� ��������� � ����, ����� �������������������� � SHA-1 �� ���� ����� � ���������� ������ � ���� input (����. �����) ������ �������, ����� ��� ����������� � ������������, ��� �������� ��� � ���� output (����. ������).

**��� � �������� ������������� �������**

Git ������ ������� ������������ ��� > ���������� � �������. ���� �� ������ ���, �� ������ ������ �� ���������: ������ � ���� ������� � ���������� ������������� ������. ����� �������, ��� ��� � �������� ������������� �������.

��� ������ � Git ���� ����� ����������� ��� ���������. �� ����� ����� ���������� � �������� ��������� ������ Git-��������, ����� �������, � ����� �������� ����� ���������� �� ��� ���� ��������.

��� ���� � ������� ��� > ���������� � ������� Git ��������� � ��������� �����. ��� ��������� � ������� ����� .git � ����������� �������.

## ��������� ���

������� ��������, �� ������� ������� ��������:
* ������ �� ���� � ��������� ���� ����� ����� commit � ��� ��� �������;
* Author � ��� ������ � ��� ����������� �����;
* Date � ���� � ����� �������� �������;
* � ����� ��������� ��������� �������.

��� �������� �������� �������:

```
commit e83c5163316f89bfbde7d9ab23ca2e25604af290
Author: Linus Torvalds <torvalds@linux-foundation.org>
Date:   Thu Apr 7 15:13:13 2005 -0700

    Initial revision of "git", the information manager from hell 
```

### �������� ����������� ��� � **git log --oneline**

� ��������� �������� ������ ������ ��������� �������� ���� ������� ������� � �� �����������.

����������� ��� �������, ���� � ����������� ��� ����� �������� � ��������, ����� ��� ������. � ���� ������ ����� ������ ����� ������ �� ��������.

����������� ��� (�� ���� ������ ��������� �������� �������) ����� ������������ ����� ��� ��, ��� � ������. ��� ����� ������� git log --oneline ������������� ��������� ����� ����� ����������� �����, ����� ��� ���� ����������� � �������� ����������� � Git ������ ��� ������, � ����� ������� ��� ����.

## HEAD - ����� ������

��� ������ ������� git log �� ����� ����� �������� ������� (HEAD -> master) ����� ���� ������ �� ��������

���� `HEAD` (����. �������, ���������) � ���� �� ��������� ������ ����� `.git`. �� ��������� �� ������, ������� ������ ��������� (�� ���� �� ����� �����).
� ���� ����� ��������� � ������� ���������. ��������� � ����� `.git` �������� `cd`. ���������� ���������� ����� `HEAD` �������� `cat`.

```
$ pwd # ����������, ��� ��
/Users/user/dev/first-project

$ cd .git/
$ ls # ����������, ����� ���� �����
COMMIT_EDITMSG  ORIG_HEAD  description  index  logs/     refs/
HEAD            config     hooks/       info/  objects/

$ cat HEAD # ������� cat ���������� ���������� �����
ref: refs/heads/master # � ����� ��� ����� ������ 
```

������ HEAD � ������ �� ��������� ����: refs/heads/master (��� refs/heads/main � ����������� �� �������� �����). ���� ��������� � ���� ����, ����� ������� ��� ���������� �������.

```
$ cat refs/heads/master # ����� ������ �� ����� HEAD
# ������ ���
e007f5035f113f9abca78fe2149c593959da5eb7

$ git log 
# ������� � ����� ���������� �������
commit e007f5035f113f9abca78fe2149c593959da5eb7
Author: John Doe <johndoe@example.com>
Date:   Tue Mar 28 00:26:53 2023 +0300

    �������� ������� � ������ ���

... # ������ ������� 
```
����� �� ������� ������, Git ��������� refs/heads/master � ���������� � ���� ��� ���������� �������. ����������, ��� HEAD ���� �����������, ��� ��� ��������� �� refs/heads/master.
��� ������ � Git ��������� HEAD ������������ �������� �����. �� ��� ���������, ��� ������ ������� Git ��������� � �������� ��������� ��� �������. ���� ����� �������� ��������� ������, �� ������ ��� ���� ����� ������ �������� ����� HEAD � Git �����, ��� �� ����� � ���� ��������� ������.

����� .git �������� ����� ���������� ������ � �� ����� �� ��� �� ���������� � ���� �����. ���������:
* � ����� ������ ������ � ����� .git ���� ��������� ���� HEAD. �� ��������� �� ����� ������ ������.
* ������ ���� ���������� ������� ����� �������� ����� HEAD � Git ��� �����.


## C������ ������ Git

###������� untracked/tracked, staged � modified

���� �� �������� ����� Git � ����������� ��������� ������ � �����������. ��� ����� ������ ���� ���������� �����-���� ��������

* untracked (����. ����������������)

  �� ��������, ��� ����� ����� � Git-����������� ���������� ��� untracked, �� ���� ���������������. Git ������, ��� ����� ���� ����������, �� �� ������ �� ����������� � ���. � untracked-����� ��� ���������� ������, ��������������� � �������� ��� ����� ������� git add.

* staged (����. ���������������)
  
  ����� ���������� ������� git add ���� �������� � staging area (�� ����. stage � ������, ����� [��������]� � area � ���������), �� ���� � ������ ������, ������� ������ � ������. � ���� ������ ���� ��������� � ��������� staged.
  � ����� �� ���������� ������ �� �������� ������ � �����������. ����� ������� ��� �������� � �������, ��� ������� git add ��������� ���������� (������� ���������� ����� ��� ���������� ������) �� ����� (����. stage) ��� ����� ����������, � git commit ������ ������ ���� ����� �������.

  **Staging area, index � cache**
  Staging area ����� �������� index (����. ��������) ��� cache (����. �����), � ��������� ����� staged ������ �������� indexed ��� cached.
  ��� ��� �������� ����� ����������� � ������������ � � �������� ������ ������ Git. � ����� � ��������� � ��������, � �������� � ������� �� ����� Stack Overflow.

* tracked (����. ��������������)

  ��������� tracked � ��� ����������������� untracked. ��� �������� ������� �� ������: � ���� �������� �����, ������� ��� ���� ������������� � ������� git commit, � ����� �����, ������� ���� ��������� � staging area �������� git add. �� ���� ��� �����, � ������� Git ��� ��� ����� ����������� ���������.
* modified (����. �����������)

  ��������� modified ��������, ��� Git ������� ���������� ����� � ��������� ����������� ������� � ����� �������. ��������, ���� ��� ���������� � ����� ����� �������.

**! ��� ������ � ���������� staged � modified ������ �� ���������, ��� ��� ����� tracked, ������ ��� ��� ��������� ���������������.**

### ��� staged � modified

������� git add ��������� � staging area ������ ������� ���������� �����. ���� ��, ��������, �������� git add file.txt, � ����� �������� file.txt, �� ����� ���������� ����� �� ����� ���������� � staging.
Git ������� �� ���� � ������� ������� modified: ���� ������� ������������ ��� ������, ������� ��� � staging. ����� �������� � staging ��������� ������, ����� ��������� git add file.txt ��� ���.

### �������� ��������� ���� ����� � Git
����� ����������, ��� ����� � ����������� �������� � ������ ��������� ��������. �� �������� ��� �� ���, � � ����������� ������ ������ ������������� ����.

��������� ������� ������ mermaid:
* flowchart TD ����-����� ���������
* graph LR - ������� ������������ �����


```mermaid
flowchart TD
A["untracked (���������������)"] -- git add --> B["staged (� ������ �� ������)"];
C["modified (����������)"] -- git add --> B;
B -- git commit --> D["tacked (�������������)"]
D -- ��������� --> C
```

1. ���� ������ ��� �������. Git ��� �� ����������� ���������� ����� �����. ���������: untracked.
2. ���� �������� � staging area � ������� git add. ���������: staged (+ tracked).

  * ��������, �������� ���� ��� ���. ���������: staged, modified (+ tracked).
  
    �������� ��������: staged � modified � ������ �����, �� � ������ ��� ������.

  * ��� ��� ��������� git add. ���������: staged (+ tracked).

3. ������� ������ � ������� git commit. ���������: tracked.
4. �������� ����. ���������: modified (+ tracked).
5. ����� �������� � staging area � ������� git add. ���������: staged (+ tracked).
6. ������� ������. ���������: tracked.
7. ��������� ������ 4 - 7 �����-����� ���.

������:
* �������� untracked ���������� ����, � ������������� �������� Git �����, �� �� ������ �� ����������� � ���. ���� ������ � ����������������� tracked, � ������� �������� ��� �����, ������������� Git.
* ���� ��������� � ������ staged ����� ���������� git add.
* ������ modified ��������, ��� ���� ��� �������.
* ����������� ������ � �������� ������� �� ���������� �����: ��������� > ��������� � ������ �� ������ > ������������ > ��������� > � ��� �����.

## ��� ������ git status

### ����� ��������� ���������� git status

����������� ������ � �������� ������� ����� ���������� � ��������� tracked (�� ���� ����������� � �� �������� ����� �������). �� �� ������� ��� ��������� � ������ ������� git status � ����� ��� �� ������ ��� �������� ������ ������ ���� ������ �������.

� ����� git status ���������� ������ ��������� ��������� ������:
* staged (Changes to be committed � ������ git status);
* modified (Changes not staged for commit);
* untracked (Untracked files).

��������� ��, � ��� ���������� � �����:
* ������� git status ������ ���������, ��� ���������� � ������: ��������, �� �������� � ������ ��� ������ ��� ��� ������ �� �������������, ��� �������.
* git status ���������� ���� ��������� ��������� ������: untracked, staged � modified.
* git status ������������, ����� ������� ����� ���������, ����� �������� ��������� �����.
