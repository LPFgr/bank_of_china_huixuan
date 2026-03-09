---
name: "frontend-design"
description: "提供前端设计和开发功能，包括 HTML、CSS、JavaScript 等技术栈的使用。当用户需要进行前端页面设计和开发时调用。"
---

# Frontend Design

Frontend Design 技能提供了完整的前端设计和开发功能，帮助用户创建美观、响应式和交互式的网页界面。

## 核心功能

- **HTML 结构**：创建语义化的 HTML 结构，确保页面结构清晰
- **CSS 样式**：应用现代 CSS 技术，包括 Flexbox、Grid、CSS 变量等
- **JavaScript 交互**：添加动态交互效果和功能
- **响应式设计**：确保页面在不同设备上都能良好显示
- **前端框架**：支持使用 React、Vue、Angular 等前端框架
- **性能优化**：优化前端性能，提高页面加载速度
- **可访问性**：确保页面对所有用户都可访问

## 使用场景

- **网站开发**：构建完整的网站前端界面
- **Web 应用**：开发交互式 Web 应用
- **响应式设计**：创建适配不同设备的页面
- **UI/UX 设计**：设计美观且用户友好的界面
- **前端性能优化**：提高现有网站的性能

## 如何使用

1. **规划结构**：确定页面的整体结构和布局
2. **编写 HTML**：创建语义化的 HTML 结构
3. **应用 CSS**：添加样式，实现视觉效果
4. **添加交互**：使用 JavaScript 实现动态功能
5. **测试响应式**：确保在不同设备上的显示效果
6. **优化性能**：检查并优化页面加载速度
7. **确保可访问性**：测试页面的可访问性

## 示例

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>前端设计示例</title>
    <style>
        /* 基础样式 */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            color: #333;
        }
        
        /* 响应式布局 */
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* 导航栏 */
        nav {
            background-color: #333;
            color: #fff;
            padding: 10px 0;
        }
        
        nav ul {
            display: flex;
            list-style: none;
        }
        
        nav ul li {
            margin-right: 20px;
        }
        
        nav ul li a {
            color: #fff;
            text-decoration: none;
        }
        
        /* 响应式调整 */
        @media (max-width: 768px) {
            nav ul {
                flex-direction: column;
            }
            
            nav ul li {
                margin-right: 0;
                margin-bottom: 10px;
            }
        }
    </style>
</head>
<body>
    <nav>
        <div class="container">
            <ul>
                <li><a href="#">首页</a></li>
                <li><a href="#">关于我们</a></li>
                <li><a href="#">服务</a></li>
                <li><a href="#">联系我们</a></li>
            </ul>
        </div>
    </nav>
    
    <div class="container">
        <h1>欢迎来到前端设计示例</h1>
        <p>这是一个使用 HTML、CSS 和 JavaScript 构建的响应式网页示例。</p>
        
        <button id="btn">点击我</button>
        <p id="message"></p>
    </div>
    
    <script>
        // 添加交互功能
        document.getElementById('btn').addEventListener('click', function() {
            document.getElementById('message').textContent = '你点击了按钮！';
        });
    </script>
</body>
</html>
```

## 最佳实践

- **语义化 HTML**：使用正确的 HTML 标签来表达内容的含义
- **模块化 CSS**：使用 CSS 变量、BEM 命名约定等方法组织 CSS
- **可维护的 JavaScript**：使用模块化、面向对象或函数式编程方法
- **性能优化**：最小化 CSS 和 JavaScript 文件，使用适当的缓存策略
- **响应式设计**：使用媒体查询和弹性布局
- **可访问性**：遵循 WCAG 指南，确保所有用户都能访问内容
- **测试**：在不同浏览器和设备上测试页面

## 注意事项

- **浏览器兼容性**：注意不同浏览器对前端技术的支持差异
- **性能问题**：避免过度使用大型库和框架
- **安全问题**：注意防范 XSS、CSRF 等安全漏洞
- **维护性**：编写清晰、可维护的代码，添加适当的注释
- **用户体验**：关注页面的加载速度、交互响应性和整体用户体验