---
name: "python-docx"
description: "提供 Python 操作 Microsoft Word (.docx) 文件的功能，用于创建、修改和处理 Word 文档。当用户需要使用 Python 生成或处理 Word 文档时调用。"
---

# Python-docx

Python-docx 技能提供了使用 Python 操作 Microsoft Word (.docx) 文件的功能，帮助用户创建、修改和处理 Word 文档。

## 核心功能

- **文档创建**：创建新的 Word 文档
- **文本操作**：添加、修改和删除文本内容
- **格式设置**：设置字体、颜色、对齐方式等文本格式
- **段落操作**：创建和管理段落
- **表格处理**：创建、修改和填充表格
- **图片插入**：在文档中插入图片
- **样式管理**：应用和自定义文档样式
- **页眉页脚**：设置文档的页眉和页脚
- **页面设置**：调整页面大小、边距等页面属性

## 使用场景

- **报告生成**：自动生成报告文档
- **文档模板**：基于模板创建标准化文档
- **数据导出**：将数据导出为 Word 格式
- **文档处理**：批量处理和修改现有 Word 文档
- **自动化办公**：简化重复性的文档创建任务

## 如何使用

1. **安装库**：使用 pip 安装 python-docx 库
2. **导入模块**：在 Python 脚本中导入 docx 模块
3. **创建或打开文档**：创建新文档或打开现有文档
4. **操作文档内容**：添加文本、表格、图片等内容
5. **设置格式**：应用适当的格式和样式
6. **保存文档**：将修改后的文档保存到指定位置

## 示例

```python
from docx import Document
from docx.shared import Inches

# 创建新文档
doc = Document()

# 添加标题
doc.add_heading('Python-docx 示例', 0)

# 添加段落
p = doc.add_paragraph('这是一个使用 python-docx 创建的文档示例。')

# 添加带样式的文本
p.add_run(' 这是加粗文本').bold = True
p.add_run(' 这是斜体文本').italic = True

# 添加标题和段落
doc.add_heading('章节 1', level=1)
doc.add_paragraph('这是章节 1 的内容。')

# 添加表格
table = doc.add_table(rows=3, cols=3)
table.style = 'Table Grid'

# 填充表格
hdr_cells = table.rows[0].cells
hdr_cells[0].text = '姓名'
hdr_cells[1].text = '年龄'
hdr_cells[2].text = '职业'

row_cells = table.rows[1].cells
row_cells[0].text = '张三'
row_cells[1].text = '30'
row_cells[2].text = '工程师'

row_cells = table.rows[2].cells
row_cells[0].text = '李四'
row_cells[1].text = '25'
row_cells[2].text = '设计师'

# 添加图片（如果有图片文件）
# doc.add_picture('example.png', width=Inches(1.25))

# 添加分页符
doc.add_page_break()

# 添加新页面的内容
doc.add_heading('章节 2', level=1)
doc.add_paragraph('这是新页面的内容。')

# 保存文档
doc.save('example.docx')
print('文档已保存为 example.docx')
```

## 最佳实践

- **使用样式**：使用内置样式或创建自定义样式来保持文档格式一致
- **模块化代码**：将文档处理逻辑分解为函数，提高代码可维护性
- **错误处理**：添加适当的错误处理，确保文档操作的可靠性
- **性能优化**：对于大型文档，注意内存使用和处理速度
- **版本兼容性**：注意不同版本的 python-docx 可能有不同的 API

## 注意事项

- **依赖项**：python-docx 依赖 lxml 和 python-docx-core
- **文件格式**：只支持 .docx 格式，不支持 .doc 格式
- **复杂格式**：对于非常复杂的 Word 格式，可能需要使用更专业的工具
- **图片处理**：插入图片时需要注意图片路径和大小
- **表格操作**：复杂表格的操作可能需要更多的代码来处理

## 安装方法

使用 pip 安装 python-docx 库：

```bash
pip install python-docx
```