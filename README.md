# BUAAUpdateActionVer
the main python script is forked from https://github.com/windiboy/BUAAAutoUpdate

# Warning
**This repository is created just for learning, and everyone who use it should not violate relevant regulations.**

# How to use?
## Step 1
- Fork this repository. (Of course you should log in first!!!)
## Step 2
- You should get FORM_DATA first at this step.
- **The tutorial refers to [BUAAAutoUpdate](https://github.com/windiboy/BUAAAutoUpdate).**
- 使用电脑端chrome浏览器，打开并登录[北航师生报平安系统](https://app.buaa.edu.cn/site/buaaStudentNcov/index)
- 如果无法获取定位，可以参考[Chrome 自定位置](https://blog.csdn.net/u010844189/article/details/81163438)。
- 按F12打开控制台，切换到网络栏（network）。在页面中填好全部信息之后，点击提交，然后查看`network`标签中的`save`项。点击后查看`Headers`标签，点击`Form Data`右侧的`view source`，复制备用。
## Step 3
- Add four action secrets in Settings->Security->Secrets->Actions->New repository secret as follow:
![BUAAAutoUpdateSecret.jpg](https://s2.loli.net/2022/07/05/pRWwYiA4Ovx2hBZ.jpg)
- The four names are: STUDENTID, PASSWORD, SERVER_SEC, FORM_DATA
- STUDENTID is your BUAA SSO Account ID, namely your student id.
- PASSWORD is the password of your BUAA SSO Account.
- SERVER_SEC is your Wechat_Key provided by [ServerChan](https://sct.ftqq.com/). If you don't have the key, you can just fill in any legal string as its value.
- FORM_DATA is got from Step 2.
## Step 4
- Open Action in your forked repository, and you should enable the workflow named *BUAAAutoUpdate Action Ver*.
- The default configuration is scheduled to run the workflow at 16:26 (UTC +8:00) every day, and you can also run it manually as follow image in the Action page.
![BUAAAutoUpdateAction.jpg](https://s2.loli.net/2022/07/06/upgEq81INAf7YyK.jpg)
- If you want to change the scheduled time, you can edit file ./.github/workflows/main.yml at line 12.
- If you don't know how to use cron, you can refer to [this page](https://docs.github.com/cn/actions/using-workflows/events-that-trigger-workflows#schedule).

