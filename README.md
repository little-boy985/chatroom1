# chatroom1
# ☕ Java Web 简易聊天室 (v1.0 基础版)

这是一个基于原生 Java Servlet 和 JSP 开发的简易在线聊天室项目。该版本主要侧重于后端逻辑的实现，演示了基本的 WebSocket/轮询 通信原理（本例使用 AJAX 轮询或页面刷新机制）以及 Session 管理。

## 🛠 技术栈

- **服务器**: Apache Tomcat 9 (支持 Servlet 4.0)
- **核心框架**: Java EE 8 (`javax.servlet.*`)
- **前端**: JSP, HTML, CSS (基础样式), JavaScript
- **数据交互**: Form 表单提交 / 基础 AJAX
- **依赖管理**: Maven

## ✨ 功能特性

1.  **用户登录**: 输入用户名即可登录（无密码校验，主要用于绑定 Session）。
2.  **群组聊天**: 登录后进入公共聊天室，所有用户可见。
3.  **在线列表**: 显示当前在线的用户名。
4.  **消息记录**: 显示最近的历史消息。
5.  **用户退出**: 点击退出销毁 Session 并返回登录页。

## 🚀 部署说明 (Tomcat 9)

由于本项目使用旧版 `javax` 包，**必须** 部署在 Tomcat 9 或 Tomcat 8 上，Tomcat 10 会报错。

1.  **Maven 打包**:
    ```bash
    mvn clean package
    ```
2.  **配置 Tomcat**:
    - 在 IDE (IntelliJ IDEA / Eclipse) 中配置 Tomcat 9 Server。
    - 将生成的 `war` 包或 `war exploded` 部署到服务器。
3.  **运行**:
    - 启动服务器，访问 `http://localhost:8080/你的项目名/`。

## ⚠️ 注意事项

- **乱码问题**: 如果遇到乱码，请确保 `web.xml` 或 Servlet 中配置了 `UTF-8` 过滤器。
- **页面刷新**: 消息可能不是实时推送的，需要手动刷新或依赖简单的 JS 定时器。
- **界面**: 界面较为原始，仅用于功能演示。

---
