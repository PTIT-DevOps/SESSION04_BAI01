# BT01 - Khởi tạo Local Repository và Cấu hình danh tính (Git Init and Local Identity)

## 1. Khởi tạo repository cục bộ

```powershell
PS D:\Work\Rikkei\devops\BT\SS04\SS04-BT01> git init
Initialized empty Git repository in D:/Work/Rikkei/devops/BT/SS04/SS04-BT01/.git/
```

## 2. Cấu hình danh tính tác giả ở cấp local

Ràng buộc của bài là bắt buộc dùng `--local`, không dùng `--global`, để không ảnh hưởng tới cấu hình toàn cục của máy.

```powershell
PS D:\Work\Rikkei\devops\BT\SS04\SS04-BT01> git config --local user.name "lethinh"
PS D:\Work\Rikkei\devops\BT\SS04\SS04-BT01> git config --local user.email "lephuthinh387@gmail.com"

PS D:\Work\Rikkei\devops\BT\SS04\SS04-BT01> git config --local --list
core.repositoryformatversion=0
core.filemode=false
core.bare=false
core.logallrefupdates=true
core.symlinks=false
core.ignorecase=true
user.name=lethinh
user.email=lephuthinh387@gmail.com
```

## 3. Tạo tệp tin, đưa vào Staging Area và commit đầu tiên

```powershell
PS D:\Work\Rikkei\devops\BT\SS04\SS04-BT01> git status
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        README.md

nothing added to commit but untracked files present (use "git add" to track)

PS D:\Work\Rikkei\devops\BT\SS04\SS04-BT01> git add README.md
PS D:\Work\Rikkei\devops\BT\SS04\SS04-BT01> git commit -m "docs: thêm README.md cho bài tập đầu tiên"
[main (root-commit) 9d664d1] docs: thêm README.md cho bài tập đầu tiên
 1 file changed, 12 insertions(+)
 create mode 100644 README.md
```

## 4. Kiểm tra cấu hình và lịch sử commit

```powershell
PS D:\Work\Rikkei\devops\BT\SS04\SS04-BT01> git config --local user.email
lephuthinh387@gmail.com

PS D:\Work\Rikkei\devops\BT\SS04\SS04-BT01> git config --local user.name
lethinh

PS D:\Work\Rikkei\devops\BT\SS04\SS04-BT01> git log --oneline
9d664d1 (HEAD -> main) docs: thêm README.md cho bài tập đầu tiên
```
