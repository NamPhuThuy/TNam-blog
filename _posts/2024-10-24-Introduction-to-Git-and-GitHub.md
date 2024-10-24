---
title:  "Git n Github 01: Giới thiệu về Git và Github"
search: true
categories: 
  - Git_and_Github
last_modified_at: 2024-10-24T08:06:00+07:00
---

# Git và Github là gì

<div style="text-align: center"><img src="{{ site.url }}{{ site.baseurl }}/assets/images/Git-n-Github/git-github.png" alt="Git n Github" width="350px" ></div>


HIHI

{% capture fig_img %}
![Foo]({{ "../assets/images/Git-n-Github/git-github.png" | relative_url }})
{% endcapture %}



- Git:
  - Hệ thống kiểm soát phiên bản phân tán **(DVCS - distributed version control system)** 
  - Theo dõi những thay đổi trong mã nguồn (source code) trong quá trình phát triển phần mềm.
  - Cho khả năng làm việc nhóm và quay lại các phiên bản trước nếu cần

- GitHub:
  - Dịch vụ lưu trữ **Git-repository** dựa trên nền tảng web

|   | Git                             | Github                         |
|---|---------------------------------|--------------------------------|
| 1 | phần mềm                        | dịch vụ                        |
| 2 | command-line interface (CLI)    | graphical user interface (GUI) |
| 3 | quản lý lịch sử mã nguồn        | quản lý các Git repositories    |


# Basic Git Workflow
<div style="text-align: center"><img src="{{ site.url }}{{ site.baseurl }}/assets/images/Git-n-Github/git-workflow.png" alt="Git n Github" width="350px"></div>

- Working directory: nơi lưu toàn bộ file của dự án
- Staging area: vị trí tạm thời, nơi các files được lưu trữ cho lần commit tiếp theo
- Local repository: chứa các file đã được commit nằm trên local
- Remote repository: chứa các file đã được commit nằm trên remote

# Cơ bản với Git
## Chuẩn bị
Tải và cài đặt Git: 
<a href = "https://git-scm.com/downloads"> Git SCM </a>  
Tải và cài đặt Fork:
<a href = "https://git-fork.com/">Fork - git client</a>

## Basic commands
- **Cài đặt thông tin về tên và email**
```
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

- **Khởi tạo Git repository**   
Truy cập tới directory mong muốn và chạy lệnh:
```
git init
```

- **Tạo 1 file mới bất kì**
```
touch example.txt
```

- **Thêm file mới thay đổi vào Staging Area**
```
git add <filename>: Thêm file theo tên
git add .: Thêm toàn bộ file vào staging area
----
Ví dụ: git add example.txt
```

- **Kiểm tra trạng thái của repository**
```
git status
```
- **Tạo commit**: 
When you make a commit, Git stores a commit-object that contains a pointer to the snapshot of the content you staged. This object also contains the author’s name and email address, the message that you typed
```
git commit -m "<commit message>"
----
Ví dụ: git commit -m "Testing commit"
```

- **Xem lịch sử commit**
```
git log
```

## Kết nối local repository với remote repository trên Github
- **Tạo tài khoản** <b><a href = "https://github.com/">Github</a> </b>
- **Tạo Github repository**: Sau khi đăng nhập thành công, chạy lệnh này trên trình duyệt để tạo **Github-repository** mới
```
repo.new
```
- **Sao chép URL của repository vừa tạo**
```
https://github.com/<your_username>/<repository_name>.git
```

- **Kết nối local repository và remote repository**
```
git remote add origin https://github.com/<your_username>/<repository_name>.git
```

- **Kiểm tra lại kết nối đã đúng chưa**
```
git remote -v
```

- **Đẩy tài nguyên lên repository**
```
gir push <remote_name> <branch_name>
```

# Tham khảo 

<a href = "https://www.geeksforgeeks.org/difference-between-git-and-github">Difference Between Git and GitHub</a>  - Geeksforgeeks  
<a href = "https://blog.bytebytego.com/i/95179881/how-does-git-work"> How does git work? </a> - ByteByteGo