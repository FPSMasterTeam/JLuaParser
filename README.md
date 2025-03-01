# JLuaParser

[![License: GPL-3.0](https://img.shields.io/badge/License-GPL--3.0-blue.svg)](https://www.gnu.org/licenses/gpl-3.0.html)

**JLuaParser** 是一个基于纯字符串的 Lua 抽象语法树（AST）解析框架的 Java 实现。它旨在提供一个轻量级、简洁的库，用于将 Lua 代码解析为其 AST 结构，供其他程序进行分析、转换和处理。

---

## 📦 特性

- **基于字符串的解析**：不依赖外部Lua引擎，通过字符串匹配实现高效解析。
- **支持标准Lua语法**：处理常见的Lua语法，包括变量声明、表达式、函数定义等。
- **AST输出**：返回解析后的抽象语法树（AST），便于进一步分析或修改Lua代码。
- **轻量级实现**：设计简单，易于集成到其他Java项目中。
- **GPL-3.0许可**：符合GPL-3.0许可证，允许修改和再发布。

---

## 🛠️ 安装

### 使用Maven

你可以通过Maven将**JLuaParser**添加到你的项目中。只需在`pom.xml`文件中添加以下依赖：

```xml
<dependency>
    <groupId>top.skidder</groupId>
    <artifactId>JLuaParser</artifactId>
    <version>1.0.0</version>
</dependency>
```

### 手动构建

1. 克隆项目：
    ```bash
    git clone https://github.com/FPSMasterTeam/JLuaParser.git
    cd JLuaParser
    ```

2. 使用Maven构建：
    ```bash
    mvn clean install
    ```

3. 你可以在本地仓库中找到构建后的JAR文件，或者将其发布到你的私有仓库。

---

## ⚡ 使用示例

以下是如何在Java中使用**JLuaParser**的简单示例：

```java
import top.skidder.lua.parser.LuaParser;
import top.skidder.lua.ast.LuaAST;

public class LuaParserExample {
    public static void main(String[] args) {
        String luaCode = "local a = 10\nlocal b = 20\nreturn a + b";

        // 解析Lua代码
        LuaParser parser = new LuaParser();
        List<Statement> ast = parser.parse(luaCode);

        // 输出AST
        for(Statement statement : ast) {
            System.out.println(statement.toString());
        }
    }
}
```

在这个示例中，我们解析了一段简单的Lua代码，返回的结果是该代码的AST结构。

---

## 🔧 贡献

1. **Fork** 本仓库
2. 创建你自己的分支：`git checkout -b feature-branch`
3. 提交更改：`git commit -am 'Add new feature'`
4. 推送到分支：`git push origin feature-branch`
5. 创建一个新的Pull Request

---

## 📃 许可证

**JLuaParser** 使用 [GPL-3.0](https://www.gnu.org/licenses/gpl-3.0.html) 许可证。可以自由使用、修改、分发，但需要遵循该许可证的条款。

---

## 📞 联系

如果有任何问题或建议，欢迎通过以下方式联系：

- GitHub Issues：[https://github.com/FPSMasterTeam/JLuaParser/issues](https://github.com/skidder-top/JLuaParser/issues)
- 电子邮件：[SuperSkidder@proton.me](mailto:SuperSkidder@proton.me)

---

**JLuaParser** 是一个由 **FPSMasterTeam** 维护的开源项目。
