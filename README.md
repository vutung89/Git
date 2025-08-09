# Git
- git status
- git remote -v
- git fetch origin
- git brach -r
- git add <ten_file>
- git commit -m "noi dung"
- git push origin <nhanh muon push>
## Nếu đang ở repo cũ nhưng muốn đổi remote sang repo khác
Ví dụ: bạn đang ở thư mục repo A, nhưng muốn nó trỏ sang private repo B trên GitHub
```bash
git remote set-url origin https://github.com/username/private-repo-khac.git
```

##  Cách xử lý để sang dev mà vẫn giữ được thay đổi
1. Lưu tạm thay đổi hiện tại (stash)
```bash
git add .                  # lưu tất cả file modified vào index
git stash                  # lưu tạm vào stash
git checkout -b dev origin/dev   # sang branch dev
git stash pop     
```
## Nếu muốn lấy bản file từ branch khác (VD: main) sang dev rồi push
- Đang ở branch dev
```bash
git checkout main -- <ten_file>
git commit -m "Cập nhật file từ main sang dev"
git push origin dev
```