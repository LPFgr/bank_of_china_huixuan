---
name: "html-to-figma"
description: "提供将 HTML 转换为 Figma 设计的功能，用于将网页代码转换为 Figma 可编辑的设计文件。当用户需要将现有网页转换为 Figma 设计以便进一步编辑和设计时调用。"
---

# HTML-to-Figma

HTML-to-Figma 技能提供了将 HTML 转换为 Figma 设计的功能，帮助用户将网页代码转换为 Figma 可编辑的设计文件。

## 核心功能

- **HTML 分析**：分析 HTML 结构和样式
- **Figma 转换**：将 HTML 元素转换为 Figma 组件
- **样式保留**：保留原始 HTML 的样式和布局
- **组件识别**：识别和转换常见的 UI 组件
- **响应式布局**：处理响应式布局和断点
- **交互元素**：转换交互元素和状态

## 使用场景

- **设计迁移**：将现有网页转换为 Figma 设计
- **设计系统构建**：基于现有网页构建设计系统
- **设计迭代**：在现有网页基础上进行设计迭代
- **团队协作**：将开发代码转换为设计文件以便设计团队编辑
- **设计文档**：为现有网页创建设计文档

## 如何使用

1. **输入 HTML**：提供 HTML 代码或网页 URL
2. **分析处理**：系统分析 HTML 结构和样式
3. **转换设置**：设置转换选项和参数
4. **生成 Figma 文件**：系统生成 Figma 设计文件
5. **导入 Figma**：将生成的文件导入到 Figma 中
6. **编辑优化**：在 Figma 中编辑和优化设计

## 示例

### 基本使用流程

1. **输入 HTML**：输入 HTML 代码或网页 URL
   ```html
   <div class="container">
     <header>
       <h1>Welcome to our website</h1>
       <nav>
         <ul>
           <li><a href="#">Home</a></li>
           <li><a href="#">About</a></li>
           <li><a href="#">Services</a></li>
           <li><a href="#">Contact</a></li>
         </ul>
       </nav>
     </header>
     <main>
       <section>
         <h2>About Us</h2>
         <p>We are a team of dedicated professionals.</p>
       </section>
     </main>
   </div>
   ```

2. **设置转换选项**：选择需要转换的元素和样式
3. **生成 Figma 文件**：系统生成 Figma 设计文件
4. **导入到 Figma**：将生成的文件导入到 Figma 中进行编辑

## 最佳实践

- **干净的 HTML**：使用结构清晰、语义化的 HTML
- **内联样式**：对于重要样式，使用内联样式以确保正确转换
- **组件化结构**：使用组件化的 HTML 结构以便更好地转换为 Figma 组件
- **响应式设计**：明确标记响应式断点以便正确转换
- **测试验证**：在转换后验证 Figma 文件的准确性

## 注意事项

- **复杂布局**：复杂的布局可能需要手动调整
- **动态内容**：动态生成的内容可能无法完全转换
- **外部资源**：外部 CSS 和 JavaScript 可能影响转换效果
- **Figma 限制**：Figma 的某些限制可能影响转换结果
- **性能考虑**：大型 HTML 文件可能需要较长的转换时间

## 技术原理

1. **HTML 解析**：解析 HTML 结构和 DOM 树
2. **样式提取**：提取和分析 CSS 样式
3. **元素映射**：将 HTML 元素映射到 Figma 元素
4. **布局计算**：计算元素的位置和大小
5. **Figma API**：使用 Figma API 创建和组织设计元素
6. **文件生成**：生成 Figma 可导入的文件格式