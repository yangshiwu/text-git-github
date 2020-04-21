### 个人开发应用git


第一步 : 在需要git 管理的文件夹下打开git base here 
第二步：在git中进行项目管理的初始化 git init
第三步：在git中创建自己的项目文件
第四步：通过git add * 将所有的项目文件添加进去临时区域内
第五步：通过git commit -m 操作说明  将临时区域内的项目推送到本地的仓库上去
第六步：对项目进行修改之后,可以先看看修改了哪些东西，git diff 
第七步：确认完修改之后，可以通过git commit -a -m 操作说明 来进行上传了.
第八步：如果需要切换版本，只需要通过git reflog 查看下自己的操作历史，然后通过git reset 
--hard 版本号 就可以自由的切换不同的状态了。
第九步: 如需删除文件，使用git rm 文件名 来进行删除,然后通过git commit -a -m 提交
第十步:如果发生在本地误删的情况，可以直接使用git checkout 把临时区域的内容拉到本地


### 合作开发
1：创建本地的ssh秘钥  作用：告诉远程仓库  是你自己推送的消息
~~~

$ ssh-keygen -t rsa -C "949012665@qq.com"


查看公钥
$ cat ~/.ssh/id_rsa.pub
~~~

ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABgQDgnkQt2HQyig1nLCt2RNdrVQN3AzxPUZkbkuNBMMkLrJ6WEiZKTg17lWrQGc3sURKmBztqfI1gFQ2JyaP6+7OPpIRUk5ZFsf+Zqk+GIGFZunJSXk8345x5G8t5fKxKNWR6kMwdTnIg+QN1So7JL2IuTG0NrHU/kM2ufDmmAy6ztn9JlrAS4IiCCb2GeDAtmVkGPTlNT77zvSyijCJqavWb34eaxsQ3louHF2WhKMmWNhlxdGl/shVvPWpTPnghQmi6k5Kxb2hwZsgbqMkNXTgRzkZQWfdaBiCN/Z8a3i7Tc3CCZW31XAdo1FHJJatQofDV0Dx+ZwqBLWDuQZ/cunrP4Ua1JguNWsLHgC0+3YR1NYaO6uoVEYRDyqRVlAwZWNiGBKbtaZQI2gwGRpq9gN0X5ODwIiucG7yj/7dmYfFyrczDRNt4kW58wjZA2JUXwzD5G6GL2WYYg+Pe3edctHwqgq6EVyvxHm/RMYluHtBZ85v+PFj7uVCTKHspZzSk+Ck= 949012665@qq.com
