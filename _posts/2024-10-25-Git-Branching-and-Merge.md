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

**Branching** hay phân nhánh, có nghĩa là **tách khỏi luồng chính**. Mục đích để quá trình xây  dựng tính năng mới không làm ảnh hưởng tới luồng chính


## Tạo nhánh
- **Tạo 1 nhánh mới**: 
```
git branch <branch_name>
```

- **Git switch và git checkout**

|                     | git switch                                   | git checkout                                                                                      |
|---------------------|----------------------------------------------|---------------------------------------------------------------------------------------------------|
| Mục đích            | Chuyển nhánh: ```git switch <branch_name>``` | Chuyển nhánh: ```git checkout <branch_name>``` <br/>Tạo nhánh: ```git checkout -b <branch_name>``` |

- **Hiển thị tất cả các nhánh**  
  - Hiển thị toàn bộ nhánh ở **local**
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

[//]: # (<div style="text-align: center"><img src="" alt="Git n Github" width="350px"></div>)
- **Solve conflicts**

## Git workflow when teamwork
<div style="text-align: center;"><img src="{{ site.url }}{{ site.baseurl }}/assets/images/Git-n-Github/git-workflow-teamwork.png" alt="Git n Github" width="350px"></div>


# References 

<a href = "https://www.geeksforgeeks.org/introduction-to-git-branch">Introduction to Git Branch
</a>  - Geeksforgeeks  
<a href = "https://stackoverflow.com/questions/57265785/whats-the-difference-between-git-switch-and-git-checkout-branch">What's the difference between 'git switch' and 'git checkout' <branch>?</a> - StackOverflow