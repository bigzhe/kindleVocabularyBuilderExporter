# kindleVocabularyBuilderExporter
kindleVocabularyBuilderExporter 读取 kindle 中 Vocabulary Builder 的内容，利用 有道翻译API 进行翻译，并对单词进行格式化的导出，方便上传到 Quizlet 进行复习。

## 基本功能

- 读取 kindle 数据文件
- 根据书名现实单词
- 利用 有道翻译API 对单词进行翻译
- 单词根据格式导出，方便导入 Quizlet 进行复习

## 安装说明
Note: 如果不需要翻译功能可以直接跳到使用说明

第一次使用之前需要进行一些配置以及安装，第二次使用不需要再进行配置

1. 有道翻译API 的申请
2. 填写 有道翻译API 到程序
3. Chrome extension 的安装

#### 有道翻译API 的申请
有道翻译API 是有道公司提供的翻译和查词的数据接口，kindleVocabularyBuilderExporter 使用 有道翻译API
进行翻译。

首先打开 [有道翻译API](https://github.com/Melo618/Simple-Markdown-Guide) 的网址

http://fanyi.youdao.com/openapi?path=data-mode

填写网站名称，网站地址，网站说明以及联系方式。

![YoudaoAPI](img/youdao_api_application.png)

申请成功之后，请保存 __API Key__ 和 __keyfrom__

#### 填写 有道翻译API 到程序

使用文本编辑工具打开 index.html，Windows 可以使用 记事本，Mac 可以下载免费的 Sublime 等

![Open index.html](img/open_index.png)

打开后找到大约108行

![YoudaoAPI](img/edit.png)

把 __API Key__ 和 __keyfrom__ 输入进去，并保存文件

![YoudaoAPI](img/edited.png)

#### Chrome extension 的安装

由本地浏览器访问有道网页并拿到翻译时候，chrome浏览器默认这是一个不安全的行为，会阻止翻译传进来，所以要安装一个chrome插件防止翻译被阻止

打开Chrome的插件页：把 URL `chrome://extensions` 复制到地址栏 或是点击 Menu > Settings > Extensions 都可以。

![Chrome](img/chrome_extension.png)

将 `Allow-Control-Allow-Origin_--_v1.0.3.crx` 文件拖拽到 Chrome Extensions 页面

![Chrome](img/drag.png)

点击确定进行安装即可

## 使用说明
程序的使用大致分成四个阶段

1. 导入 kindle 数据库文件
2. 选择要导出的书籍
3. 确认 有道翻译API 已经成功申请并填写
4. 对该书单词进行翻译或导出
5. 将导出的单词导入 Quizlet
