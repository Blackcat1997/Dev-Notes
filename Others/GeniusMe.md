### 🦠 

### 更改密码之后，重启系统输入新密码无法登录

💊  

- 开机长按command + S

- 进入单用户模式

- 输入命令

  - 对文件系统检查修复

    ```shell
    fsck -y
    ```

  - 挂载分区

    ```shell
    mount -uaw /
    ```

  - 删除系统安装完毕的配置

    ```shell
    rm /var/db/.AppleSetupDone
    ```

  - 重启

    ```shell
    reboot
    ```

    

  