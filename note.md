# 這裡是筆記區域

刪除本機端的git: 直接把隱藏的資料夾「.git」移除、再重新建立repository即可。
<br>ref: https://stackoverflow.com/questions/1213430/how-to-fully-delete-a-git-repository-created-with-init 

建立local git repository: 
```powershell
# 將工作目錄(working directory)移置想建立repository的資料夾底下
cd "/path_to_your_local_directory" 
git init -b main                # 建立名為main的branch與local git repository
git add file.extention          # 將更新的file.extention加入git儲列
git commit -m "first commit"    # 把所有位於git儲列的檔案更新至git紀錄
git remote add origin URL       # 連線到remote端repository的URL
git push -u origin main         # 第一次將本機端的git紀錄推送到remote端repository的branch(main)
git push                        # 第一次之後的push方式
```

```powershell
git branch develop          # 建立新的branch
git checkout develop        # 工作目錄轉換至branch
git branch                  # 查看本機端目前的所有branch
git branch -a               # 查看remote端目前的所有branch
git push -u origin develop  # 第一次將本機端的git紀錄推送到remote端repository的branch(develop)
git push                    # 第一次之後的push方式
```
將develop中開發完成的檔案merge到main當中
```powershell
git checkout main   # 工作目錄轉至main
git merge develop   # 將develop的檔案merge到main
git branch -m master main   # 將工作目錄master改名為main
```
或是使用網頁版的作法
