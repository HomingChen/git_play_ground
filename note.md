# 這裡是筆記區域

刪除本機端的git: 直接把隱藏的資料夾「.git」移除、再重新建立repository即可。
<br>ref: https://stackoverflow.com/questions/1213430/how-to-fully-delete-a-git-repository-created-with-init 

建立local git repository: 
```powershell
# 將工作目錄(working directory)移置想建立repository的資料夾底下
cd "/path_to_your_local_directory" 
git init                        # 建立local git repository
git add file.extention          # 將file.extention加入git紀錄中
git commit -m "first commit"    # 類似遊戲存檔的概念
git remote add origin URL       # 連線到remote端repository的URL
git push                        # 將本機端的git紀錄推送到外部repository
```

```powershell
git branch develop  # 建立新的branch
git checkout develop    # 工作目錄轉換至branch
git branch              # 查看本機端目前的所有branch
git branch -a           # 查看remote端目前的所有branch
```