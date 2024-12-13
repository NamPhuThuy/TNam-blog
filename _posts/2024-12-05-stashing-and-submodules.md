---
title:  "Git n Github 04: Stash và Submodule"
search: true
categories: 
  - Git_and_Github
last_modified_at: 2024-12-05T17:26:00+07:00
---

Git stash and submodule

# Stashing
- Là cách tạm thời để lưu các thay đổi đã thực hiện nhưng chưa sẵn sàng để commit.
- Dùng khi muốn chuyển sang nhánh khác nhưng chưa muốn commit ở nhánh hiện tại

## Practice
- Tạo git repository
```
git init
```

- Tạo file mới 
```
touch a.txt
```

- Tạo commit với file này
```
git add, git commit
```

- Sửa dữ liệu của file vừa commit
```
echo <new_content> > a.txt
vd: echo "something" > a.txt
```

- Đưa những thay đổi vào phần stash
```
git stash
```

- Lấy stash mới nhất ra khỏi stack
```
git stash pop
```

- Lấy thông tin của 1 stash cụ thể (nhưng không lấy khỏi stack) 
```
git stash apply stash@{<stash_id>}
vd: git stash apply stash{0}
```

- Hiển thị danh sách stash 
```
git stash list
```

- Xóa đi 1 stash cụ thể
```
git stash drop stash@{1}
```
# Submodules



## Practice
- Thêm kéo 1 repo trên mạng về làm submodule của repo hiện tại 
```
git submodule add <repository_url> <path/to/submodule>
vd: git submodule add https://github.com/NamPhuThuy/Python-Pygame.git
```

- Clone 1 project có chứa submodule
```
git submodule init  # Initialize the submodules
git submodule update  # Clone the submodule repositories
```

- Submodule foreach: thực hiện 1 lệnh cụ thể trên từng submodule
```
git submodule foreach git pull origin main
```

- Recursive cloning
```
git clone --recurse-submodules <repository_url>
vd: git clone --recurse-submodules https://github.com/NamPhuThuy/Python-101
```

- Kiểm tra trạng thái của từng submodule
```
git submodule state
```