# BJTU-course-autoget
北京交通大学自动选课软件，`python`自动化网络请求，高效稳定。

**！！！我们的目标是帮助每一个因课程交易而受影响的学生选择他们心仪的课程，并且我们强烈谴责买卖课程和囤积课程以出售的行为。**

## 依赖

这个Python脚本的依赖项包括以下库：

1. `requests`：用于发出网络请求，如GET和POST。
2. `json`：用于处理JSON格式的数据。
3. `re`：正则表达式库，用于处理和匹配字符串。
4. `base64`：用于进行Base64编码和解码。
5. `time`：用于处理时间和延迟。
6. `BeautifulSoup`：用于解析和处理HTML文档。
7. `tqdm`：用于添加一个进度提示信息 

你可以使用pip来安装这些依赖库，使用下面的命令：

```bash
pip install requests beautifulsoup4 tqdm
```

其他的库如`json`，`re`，`base64`和`time`都是Python内置的，无需额外安装。



## 食用方法

这是一个抢课脚本的Python代码，旨在自动帮助用户在北京交通大学的课程选择系统中抢课。但是，请注意使用此类脚本可能违反学校的使用条款和政策，因此在使用前请仔细考虑可能的后果。此外，此脚本需要用户具备一定的Python编程知识才能正确使用。

以下是这个脚本的大概使用方法：

1. **配置个人信息**：你需要在脚本中提供自己的学号（`user_id`），密码（`user_password`），以及要抢的课程列表（`course_list`）。同时，你还需要提供图鉴验证码API的用户名（`tujian_uname`）和密码（`tujian_pwd`）以解析登录时的验证码。请注意，你需要在[图鉴官网](http://www.ttshitu.com/)注册并购买API使用权限。
2. **运行脚本**：一旦你提供了所有必要的信息，你就可以运行这个脚本。它首先会登录到北京交通大学的网站，并获取用于后续操作的cookie。
3. **获取所有课程信息**：脚本会从北京交通大学的网站上获取所有课程的信息，并筛选出你想要抢的课程。
4. **抢课**：脚本会持续尝试选择你想要的课程，直到成功或达到设定的重试次数（`RETRY_LIMIT`）。每次尝试都会解析新的验证码，这是通过调用图鉴API实现的。

请注意，这个脚本在抢课的过程中可能会产生大量的网络请求，可能会引起学校或网络服务提供商的注意。使用这个脚本的风险由使用者自己承担。



## 特点

1. 一旦Cookie失效，程序将自动重新登录，确保流程的连续性和完整性。
2. 不再需要手动输入验证码，提供了快速且高效的体验。
3. 全自动化的操作设计，无需亲自监督，帮你节省宝贵的时间，微信实时获取状态消息。



### p.s.

`get.py`是重构版本，但由于在重构过程中选课系统已经关闭，因此无法测试其是否可用。

`old.py`是初版代码，代码冗长丑陋，仅用于自己使用，但确保了其可用性。

两个版本都添加了解决登录和提交时验证码的方法，所以可以放心使用。

我会在之后的选课开始时及时完善各种功能，请跟进了解。

如果有任何修改建议或改进方法，请及时提出，我作为一个新手会及时进行改进。

如果不会操作或者操作中遇到问题，可以联系我解决。

**我们的目标是帮助每一个因课程交易而受影响的学生选择他们心仪的课程，并且我们强烈谴责买卖课程和囤积课程以出售的行为。**

**请注意，使用此类脚本可能会违反学校的使用条款和政策，所以在使用前请仔细考虑可能的后果。这包括可能会产生大量的网络请求，可能会引起学校或网络服务提供商的注意。使用这个脚本的风险由使用者自己承担**

