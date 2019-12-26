### Ubuntu Modules

## [对话框](./ubuntu_modules_dialogue)

##### *Made by* [AImator.com]()

本章主要介绍了在 Ubuntu 系统下如何利用模块 whiptail 实现对话框进行人机交互。

### 本节纲要

- **[消息框](#消息框)**
- **[是或否](#是或否)**
- **[信息框](#信息框)**
- **[输入框](#输入框)**
- **[密码框](#密码框)**
- **[文本框](#文本框)**
- **[菜单栏](#菜单栏)**
- **[多选列表](#多选列表)**
- **[单选列表](#单选列表)**
- **[进度条](#进度条)** 
- **[可选参数](#可选参数)**

---

### [消息框](#消息框)

#### 语法

```shell
whiptail –-msgbox \<text> \<height> \<width>
```

#### 实例

![whiptail-msgbox](https://code.aliyun.com/aimator/assets/raw/master/images/whiptail-msgbox.jpg?raw=true)

```shell
whiptail --title "Example Dialog" --msgbox "This is an example of a message box. You must hit OK to continue." 8 78
```

### [是或否](#是或否)

#### 语法

```shell
whiptail --yesno  <text> <height> <width>
```

#### 实例

![whiptail-yesno](https://code.aliyun.com/aimator/assets/raw/master/images/whiptail-yesno.jpg?raw=true)

```shell
# If you cannot understand this, read Bash_Shell_Scripting#if_statements again.
if (whiptail --title "Example Dialog" --yesno "This is an example of a yes/no box." 8 78) then
    echo "User selected Yes, exit status was $?."
else
    echo "User selected No, exit status was $?."
fi
```

### [信息框](#信息框)

#### 语法

```
whiptail --infobox <text> <height> <width>
```

#### 实例

```
whiptail --title "Example Dialog" --infobox "This is an example of an info box." 8 78
```

### [输入框](#输入框)

#### 语法

```shell
whiptail --inputbox <text> <height> <width> [init] 
```

#### 实例

![whiptail-inputbox](https://code.aliyun.com/aimator/assets/raw/master/images/whiptail-inputbox.jpg?raw=true)

```shell
COLOR=$(whiptail --inputbox "What is your favorite Color?" 8 78 Blue --title "Example Dialog" 3>&1 1>&2 2>&3)

# A trick to swap stdout and stderr.
# Again, you can pack this inside if, but it seems really long for some 80-col terminal users.
exitstatus=$?
if [ $exitstatus = 0 ]; then
    echo "User selected Ok and entered " $COLOR
else
    echo "User selected Cancel."
fi

echo "(Exit status was $exitstatus)"
```

### [密码框](#密码框)

#### 语法

```shell
whiptail --passwordbox <text> <height> <width> [init]
```

#### 实例

![whiptail-passwordbox](https://code.aliyun.com/aimator/assets/raw/master/images/whiptail-passwordbox.jpg?raw=true)

```shell
PASSWORD=$(whiptail --passwordbox "please enter your secret password" 8 78 --title "password dialog" 3>&1 1>&2 2>&3)

# A trick to swap stdout and stderr.
# Again, you can pack this inside if, but it seems really long for some 80-col terminal users.
exitstatus=$?
if [ $exitstatus = 0 ]; then
    echo "User selected Ok and entered " $PASSWORD
else
    echo "User selected Cancel."
fi

echo "(Exit status was $exitstatus)"
```

### [文本框](#文本框)

#### 语法

```
whiptail --textbox <file> <height> <width>
```

#### 实例

![whiptail-textbox](https://code.aliyun.com/aimator/assets/raw/master/images/whiptail-textbox.jpg?raw=true)

```
echo "Welcome to Bash $BASH_VERSION" > test_textbox
# filename height width
whiptail --textbox test_textbox 12 90
```

### [菜单栏](#菜单栏)

#### 语法

```shell
whiptail --menu <text> <height> <width> <listheight> [tag item] ...
[ ] . . .
```

#### 实例

![whiptail-menu](https://code.aliyun.com/aimator/assets/raw/master/images/whiptail-menu.jpg?raw=true)

```shell
whiptail --title "Menu example" --menu "Choose an option" 25 78 16 \
"<-- Back" "Return to the main menu." \
"Add User" "Add a user to the system." \
"Modify User" "Modify an existing user." \
"List Users" "List all users on the system." \
"Add Group" "Add a user group to the system." \
"Modify Group" "Modify a group and its list of members." \
"List Groups" "List all groups on the system."
```

### [多选列表](#多选列表)

#### 语法

```shell
whiptail --checklist <text> <height> <width> <listheight> [tag item status]...
```

#### 实例

![whiptail-checklist](https://code.aliyun.com/aimator/assets/raw/master/images/whiptail-checklist.jpg?raw=true)

```shell
whiptail --title "Check list example" --checklist \
"Choose user's permissions" 20 78 4 \
"NET_OUTBOUND" "Allow connections to other hosts" ON \
"NET_INBOUND" "Allow connections from other hosts" OFF \
"LOCAL_MOUNT" "Allow mounting of local devices" OFF \
"REMOTE_MOUNT" "Allow mounting of remote devices" OFF
```

### [单选列表](#单选列表)

#### 语法

```shell
whiptail --radiolist <text> <height> <width> <listheight> [tag item status]...
```

#### 实例

![whiptail-radiolist](https://code.aliyun.com/aimator/assets/raw/master/images/whiptail-radiolist.jpg?raw=true)

```shell
whiptail --title "Radio list example" --radiolist \
"Choose user's permissions" 20 78 4 \
"NET_OUTBOUND" "Allow connections to other hosts" ON \
"NET_INBOUND" "Allow connections from other hosts" OFF \
"LOCAL_MOUNT" "Allow mounting of local devices" OFF \
"REMOTE_MOUNT" "Allow mounting of remote devices" OFF
```

### [进度条](#进度条)

#### 语法

```shell
whiptail --gauge <text> <height> <width> <percent>
```

#### 实例

![whiptail-gauge](https://code.aliyun.com/aimator/assets/raw/master/images/whiptail-gauge.jpg?raw=true)

```shell
{
    for ((i = 0 ; i <= 100 ; i+=5)); do
        sleep 0.1
        echo $i
    done
} | whiptail --gauge "Please wait while we are sleeping..." 6 50 0
```

### [可选参数](#可选参数)

Parameter | Description
--------- | -----------
\-\-clear | clear screen on exit
\-\-defaultno | default no button
\-\-default\-item \<string\> | set default string
\-\-fb, \-\-fullbuttons | use full buttons
\-\-nocancel | no cancel button
\-\-yes\-button \<text\> | set text of yes button
\-\-no\-button \<text\> | set text of no button
\-\-ok\-button \<text\> | set text of ok button
\-\-cancel\-button \<text\> | set text of cancel button
\-\-noitem | don't display items
\-\-notags | don't display tags
\-\-separate\-output | output one line at a time
\-\-output\-fd \<fd\> | output to fd, not stdout
\-\-title \<title\> | display title
\-\-backtitle \<backtitle\> | display backtitle
\-\-scrolltext | force vertical scrollbars
\-\-topleft | put window in top-left corner
\-h, \-\-help | print this message
\-v, \-\-version | print version information
