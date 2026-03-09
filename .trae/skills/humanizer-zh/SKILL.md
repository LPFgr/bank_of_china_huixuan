---
name: "humanizer-zh"
description: "提供中文文本人性化处理功能，用于将数据转换为更自然、易读的中文表达。当用户需要处理日期、时间、数字、文件大小等数据的中文表达时调用。"
---

# Humanizer-zh

Humanizer-zh 技能提供了中文文本人性化处理功能，帮助用户将各种数据类型转换为更自然、易读的中文表达。

## 核心功能

- **日期时间处理**：将日期时间转换为自然的中文表达，如"3天前"、"刚刚"等
- **数字处理**：将数字转换为中文表达，如"一万两千三百四十五"
- **文件大小**：将文件大小转换为易读的中文表达，如"1.5MB"
- **时间跨度**：将时间跨度转换为自然的中文表达，如"2小时30分钟"
- **复数处理**：根据数量自动处理中文复数形式
- **序号处理**：将数字转换为中文序号，如"第一"、"第二"等

## 使用场景

- **用户界面**：在界面上显示更自然的时间、数字等信息
- **报告生成**：生成更易读的中文报告
- **消息通知**：发送更自然的中文通知消息
- **数据可视化**：在图表和数据展示中使用更易读的中文表达
- **国际化应用**：为中文用户提供更友好的文本表达

## 如何使用

1. **安装库**：使用 npm 或其他包管理器安装 humanizer-zh 库
2. **导入模块**：在代码中导入 humanizer-zh 模块
3. **调用相应方法**：使用库提供的方法处理数据
4. **获取人性化表达**：使用处理后的结果

## 示例

### 日期时间处理

```javascript
const humanizer = require('humanizer-zh');

// 相对时间
const date = new Date();
date.setHours(date.getHours() - 3);
console.log(humanizer.relativeTime(date)); // 输出: "3小时前"

// 时间跨度
const start = new Date();
const end = new Date();
end.setMinutes(end.getMinutes() + 45);
console.log(humanizer.duration(start, end)); // 输出: "45分钟"
```

### 数字处理

```javascript
const humanizer = require('humanizer-zh');

// 中文数字
console.log(humanizer.numberToChinese(12345)); // 输出: "一万两千三百四十五"

// 序号
console.log(humanizer.ordinal(5)); // 输出: "第五"

// 文件大小
console.log(humanizer.fileSize(1536)); // 输出: "1.5KB"
```

### 复数处理

```javascript
const humanizer = require('humanizer-zh');

// 复数形式
console.log(humanizer.pluralize(1, '苹果')); // 输出: "1个苹果"
console.log(humanizer.pluralize(3, '苹果')); // 输出: "3个苹果"
console.log(humanizer.pluralize(0, '苹果')); // 输出: "0个苹果"
```

## 最佳实践

- **选择合适的方法**：根据具体需求选择适当的人性化处理方法
- **自定义配置**：根据项目需求自定义人性化处理的行为
- **性能考虑**：对于大量数据处理，注意性能优化
- **测试验证**：在使用前测试各种边缘情况
- **国际化支持**：如果需要支持多语言，结合其他国际化工具使用

## 注意事项

- **时区问题**：处理日期时间时注意时区设置
- **精度控制**：根据需要控制数字和时间的精度
- **边界情况**：处理极端值和特殊情况
- **兼容性**：注意不同环境下的兼容性
- **依赖项**：注意库的依赖项和版本兼容性

## 安装方法

使用 npm 安装：

```bash
npm install humanizer-zh
```

或使用 yarn 安装：

```bash
yarn add humanizer-zh
```