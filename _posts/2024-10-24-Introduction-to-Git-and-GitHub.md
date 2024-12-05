---
title:  "Git n Github 01: Giới thiệu về Git và Github"
search: true
categories: 
  - Git_and_Github
last_modified_at: 2024-10-24T08:06:00+07:00
---

# Git và Github là gì

<div style="text-align: center"><img src="{{ site.url }}{{ site.baseurl }}/assets/images/Git-n-Github/git-github.png" alt="Git n Github" width="350px" ></div>


- Git:
  - Hệ thống kiểm soát phiên bản phân tán **(DVCS - distributed version control system)** 
  - Theo dõi những thay đổi trong mã nguồn (source code) trong quá trình phát triển phần mềm.

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

- Chuyển **Text editor** mặc định thành Notepad hoặc Visual Studio Code
```
git config --global core.editor "\"C:\Windows\System32\notepad.exe\""
git config --global core.editor "\"C:\Users\<YourName>\AppData\Local\Programs\Microsoft VS Code\code.exe\""
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
git push <remote_name> <branch_name>
```

- **Clone repository từ remote**
```
git clone https://github.com/<your_username>/<repository_name>.git
```

- **Kéo những commit mới nhất trong nhánh hiện tại từ remote về local**
```
git pull
```

- **Xem thông tin về về những commit mới trên remote trước khi kéo về**
```
git fetch
```
# Tổng hợp lệnh

| Lệnh                    | Tác dụng                                            |
|-------------------------|-----------------------------------------------------|
| **Cơ bản**              |                                                     |
| git init                | Khởi tạo git repository ở local (local repo)        |
| git status              | Kiểm tra trạng thái của local repo                  |
| git add                 | Thêm file vào staging area                          |
| git commmit             | Đưa toàn bộ file trong staging area vào 1 commit    |
| git log                 | Hiển thị thông tin của các commit                   |
| **Làm việc với remote** |                                                     |
| git remote add          | Kết nối local repo với remote repo                  |
| git remote -v           | Kiểm tra những kết nối của local repo               |
| git push                | Đẩy những commit của nhánh hiện tại lên remote repo |
| git fetch               | Cập nhật thông tin của remote về local              |
| git pull                | Kéo những commit từ trên remote về local            |
| git clone               | Tạo 1 bản sao của remote repo trên local            |

# Một số key words 

| Key word       | Giải thích |
|----------------|------------|
| repository     ||
| local - remote ||
| staging area   ||
|                ||
| commit message |            |

# Tham khảo 

<a href = "https://www.geeksforgeeks.org/difference-between-git-and-github">Difference Between Git and GitHub</a>  - Geeksforgeeks  
<a href = "https://blog.bytebytego.com/i/95179881/how-does-git-work"> How does git work? </a> - ByteByteGo