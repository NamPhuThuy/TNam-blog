---
title:  "Git n Github 02: Git Branching and Merge"
search: true
categories: 
  - Git_and_Github
last_modified_at: 2024-10-25T08:06:00+07:00
---

How to làm việc với nhánh?

## Git workflow when teamwork
<div style="text-align: center;"><img src="{{ site.url }}{{ site.baseurl }}/assets/images/Git-n-Github/git-workflow-teamwork.png" alt="Git n Github" width="350px"></div>

# Nhánh là gì?
<div style="text-align: center"><img src="{{ site.url }}{{ site.baseurl }}/assets/images/Git-n-Github/git-github.png" alt="Git n Github" width="350px" ></div>

**Branching** hay phân nhánh, là việc **tách khỏi luồng chính**.  
Trong quá trình phát triển phần mềm, ta cần làm việc với nhóm khi xây dựng tính năng mới mà không lo sẽ làm ảnh hưởng tới luồng chính 

## Tạo nhánh
- **Tạo 1 nhánh mới**: 
```
git branch <branch_name>
```

- **Chuyển sang nhánh mới bằng Git switch hoặc git checkout**

|                     | git switch                                   | git checkout                                                                                      |
|---------------------|----------------------------------------------|---------------------------------------------------------------------------------------------------|
| Mục đích            | Chuyển nhánh: ```git switch <branch_name>``` | Chuyển nhánh: ```git checkout <branch_name>``` <br/>Tạo nhánh: ```git checkout -b <branch_name>``` |

- **Hiển thị tất cả các nhánh**  
  - Hiển thị toàn bộ nhánh ở **local repo**
```
git branch
```

  - Hiển thị toàn bộ nhánh ở **local và remote**
```
git branch -a
```

# Tách nhánh xong thì làm gì?
- **Gộp (merge) nhánh**  
```
git merge [<branch_name_1> <branch_name_2>,..., <branch_name_n>] 
```

- **Solve conflicts (nếu có)**

## Git workflow when teamwork
<div style="text-align: center;"><img src="{{ site.url }}{{ site.baseurl }}/assets/images/Git-n-Github/git-workflow-teamwork.png" alt="Git n Github" width="350px"></div>

# Tổng hợp

| Lệnh       | Mô tả                   |
|------------|-------------------------|
| git branch | Tạo nhánh mới           |
| git switch | Di chuyển qua nhánh khác|
| git merge  | Gộp nhánh               |

## Thực hành

Khởi tạo
```
git init
```

```
touch thanRobot.txt
git add .
git commit -m "Tao than robot"
```

```
touch chanRobot.txt
git add .
git commit -m "Tao chan robot"
```

Hiện tại đang ở nhánh main/master và cần phải tạo nhánh mới để làm tay
```
git branch create_arm
git switch create_arm
```

```
touch tayRobot.txt
git add .
git commit -m "Tao tay robot"
```

```
touch fixBug.txt
git add .
git commit -m "Fix bug tay robot"
```

Lúc này, mình đang đứng ở nhánh create_arm, cần phải đưa hết phần công việc ở create_arm sang nhánh main/master
```
git switch main <nhảy sang nhánh main>
```

Mang hết phần công việc của nhánh 'create_arm' sang nhánh 'main'
```
git merge create_arm
```

Bây giờ, những phần công việc của 'create_arm' đã nằm hết ở main

# Tham khảo 

<a href = "https://www.geeksforgeeks.org/introduction-to-git-branch">Introduction to Git Branch
</a>  - Geeksforgeeks  
<a href = "https://stackoverflow.com/questions/57265785/whats-the-difference-between-git-switch-and-git-checkout-branch">What's the difference between 'git switch' and 'git checkout'?</a> - StackOverflow