---
name: "sheetjs"
description: "提供 JavaScript 处理 Excel 和其他电子表格文件的功能，用于读取、写入和操作各种电子表格格式。当用户需要在前端或后端处理电子表格数据时调用。"
---

# SheetJS

SheetJS 技能提供了使用 JavaScript 处理 Excel 和其他电子表格文件的功能，帮助用户读取、写入和操作各种电子表格格式。

## 核心功能

- **文件格式支持**：支持 Excel (XLSX, XLSB, XLSM, XLS, XLTX, XLT), CSV, TSV, JSON, HTML 等格式
- **数据读取**：从电子表格文件中读取数据
- **数据写入**：将数据写入到电子表格文件中
- **数据操作**：修改、转换和处理电子表格数据
- **样式设置**：设置单元格格式、样式和属性
- **图表支持**：处理电子表格中的图表
- **跨平台**：支持浏览器、Node.js、Deno 等环境

## 使用场景

- **数据导入导出**：在 Web 应用中导入导出 Excel 文件
- **数据处理**：处理和转换电子表格数据
- **报表生成**：基于数据生成 Excel 报表
- **数据可视化**：将电子表格数据用于可视化
- **批量数据操作**：批量处理电子表格中的数据

## 如何使用

### 浏览器环境

1. **引入库**：通过 CDN 或本地文件引入 SheetJS
2. **读取文件**：使用 FileReader 读取用户上传的文件
3. **解析数据**：使用 XLSX.read() 解析文件内容
4. **操作数据**：处理解析后的数据
5. **生成文件**：使用 XLSX.write() 生成新的电子表格文件

### Node.js 环境

1. **安装库**：使用 npm 安装 sheetjs 库
2. **导入模块**：在代码中导入 XLSX 模块
3. **读取文件**：使用 XLSX.readFile() 读取文件
4. **操作数据**：处理数据
5. **写入文件**：使用 XLSX.writeFile() 写入文件

## 示例

### 浏览器环境示例

```javascript
// 引入 SheetJS（通过 CDN）
// <script src="https://cdn.sheetjs.com/xlsx-0.19.3/package/dist/xlsx.full.min.js"></script>

// 文件上传处理
function handleFile(e) {
  const file = e.target.files[0];
  const reader = new FileReader();
  reader.onload = function(e) {
    const data = new Uint8Array(e.target.result);
    const workbook = XLSX.read(data, { type: 'array' });
    
    // 获取第一个工作表
    const firstSheetName = workbook.SheetNames[0];
    const worksheet = workbook.Sheets[firstSheetName];
    
    // 转换为 JSON
    const jsonData = XLSX.utils.sheet_to_json(worksheet);
    console.log(jsonData);
  };
  reader.readAsArrayBuffer(file);
}

// 生成 Excel 文件
function generateExcel() {
  // 示例数据
  const data = [
    { name: '张三', age: 30, city: '北京' },
    { name: '李四', age: 25, city: '上海' },
    { name: '王五', age: 35, city: '广州' }
  ];
  
  // 创建工作表
  const worksheet = XLSX.utils.json_to_sheet(data);
  
  // 创建工作簿
  const workbook = XLSX.utils.book_new();
  XLSX.utils.book_append_sheet(workbook, worksheet, 'Sheet1');
  
  // 生成并下载文件
  XLSX.writeFile(workbook, 'example.xlsx');
}
```

### Node.js 环境示例

```javascript
const XLSX = require('xlsx');

// 读取 Excel 文件
const workbook = XLSX.readFile('input.xlsx');

// 获取工作表
const sheetName = workbook.SheetNames[0];
const worksheet = workbook.Sheets[sheetName];

// 转换为 JSON
const data = XLSX.utils.sheet_to_json(worksheet);
console.log(data);

// 修改数据
data.forEach(row => {
  row.age += 1;
});

// 创建新工作表
const newWorksheet = XLSX.utils.json_to_sheet(data);

// 创建新工作簿
const newWorkbook = XLSX.utils.book_new();
XLSX.utils.book_append_sheet(newWorkbook, newWorksheet, 'Updated Sheet');

// 写入文件
XLSX.writeFile(newWorkbook, 'output.xlsx');
console.log('文件已保存为 output.xlsx');
```

## 最佳实践

- **数据处理**：使用适当的工具函数处理数据格式转换
- **性能优化**：对于大型文件，使用流式处理或分块处理
- **错误处理**：添加适当的错误处理，确保文件操作的可靠性
- **内存管理**：注意内存使用，避免处理过大的文件导致内存溢出
- **格式兼容性**：注意不同电子表格软件对格式的支持差异

## 注意事项

- **文件大小**：处理大型文件时可能会遇到性能问题
- **浏览器限制**：在浏览器环境中，文件操作受限于浏览器的安全策略
- **格式支持**：某些高级格式功能可能在不同版本的 Excel 中表现不同
- **依赖项**：在 Node.js 环境中，可能需要额外的依赖项来处理某些格式

## 安装方法

### 浏览器环境

通过 CDN 引入：

```html
<script src="https://cdn.sheetjs.com/xlsx-0.19.3/package/dist/xlsx.full.min.js"></script>
```

### Node.js 环境

使用 npm 安装：

```bash
npm install xlsx
```