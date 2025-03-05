# Cursor AI 提示词指南

## 什么是提示词 (Prompts)?
提示词是您向AI表达编码需求的自然语言指令，从简单请求到复杂任务不等。

## Cursor AI 如何使用提示词
通过理解您提示词的意图，Cursor AI 可以：
- 生成新代码片段
- 重构现有代码
- 调试并修复问题
- 创建或增强文档

## 提示词类型

### 1. 代码生成提示词
```
Create a Python function that sorts a list of integers in ascending order.
```

**响应:**
```python
def sort_numbers(numbers):
    return sorted(numbers)
```

### 2. 重构提示词
```
Optimize this JavaScript function for better performance.
```

**响应:**
```javascript
// 原始函数
function calculateSum(arr) {
    let sum = 0;
    for(let i = 0; i < arr.length; i++) {
        sum += arr[i];
    }
    return sum;
}

// 优化后的函数
function calculateSum(arr) {
    return arr.reduce((acc, curr) => acc + curr, 0);
}
```

### 3. 调试提示词
```
Identify and fix the bug in this C++ code that causes a segmentation fault.
```

**响应:**
```cpp
// 存在问题的代码
int* ptr = NULL;
*ptr = 10; // 解引用空指针

// 修复后的代码
int value = 10;
int* ptr = &value;
```

### 4. 文档提示词
```
Generate a docstring for this Java function explaining its purpose and parameters.
```

**响应:**
```java
/**
 * Calculates the factorial of a given number.
 *
 * @param n The number to calculate the factorial for.
 * @return The factorial of the number n.
 */
public int factorial(int n) {
    // 函数实现
}
```

## 有效提示词的优势
- 提高代码准确性
- 节省开发时间
- 提升代码质量
- 促进团队协作

## 撰写有效提示词的技巧

### 1. 保持明确和具体
```
// 模糊提示词
Create a login form.

// 明确提示词
Create an HTML login form with username and password fields, 
including validation and a "Remember me" checkbox.
```

### 2. 提供上下文
```
// 缺乏上下文
Fix this function.

// 有上下文
Fix this Node.js authentication function that currently 
doesn't properly validate JWT tokens.
```

### 3. 迭代改进
如果初始输出不理想，精炼您的提示词或要求调整。

### 4. 步骤化指令
```
Create a React component that:
1. Fetches data from an API
2. Displays it in a table
3. Implements pagination
4. Adds search functionality
```

## 高级提示词技巧

### 1. 使用XML结构化提示词
```xml
<task>
  <description>Create a login API endpoint</description>
  <requirements>
    <requirement>Email/password validation</requirement>
    <requirement>JWT token generation</requirement>
    <requirement>Rate limiting</requirement>
  </requirements>
  <technologies>
    <backend>Node.js, Express</backend>
    <database>MongoDB</database>
  </technologies>
</task>
```

### 2. 规则定义(Rules)
```
Generate a React component following these rules:
<rules>
1. Use functional components with hooks
2. Include PropTypes
3. Handle loading/error states
4. Use CSS modules for styling
</rules>
```

### 3. 示例与反例
```
Write a regex for valid phone numbers.

Valid: (123) 456-7890, 123-456-7890
Invalid: 12345, 123-456-78901
```

## 常见提示词模板

### 前端开发
```
Create a responsive navigation component in React that:
1. Collapses to hamburger menu on mobile
2. Has dropdown menus
3. Includes search functionality
```

### 后端开发
```
Create an Express.js API endpoint for user registration that:
1. Validates input data
2. Hashes passwords
3. Stores user in database
4. Returns appropriate status codes
```

### 数据处理
```
Write a Python function that processes a CSV file to:
1. Clean missing values
2. Calculate summary statistics
3. Generate visualization
```

## 进阶应用

### 项目规则集
```xml
<project_rules>
  <code_style>
    <indentation>2 spaces</indentation>
    <naming>camelCase for variables, PascalCase for components</naming>
  </code_style>
  <architecture>
    <pattern>Model-View-Controller</pattern>
  </architecture>
</project_rules>
```

### 多模块开发
```xml
<project>
  <module name="Authentication">
    <description>User login and registration</description>
  </module>
  <module name="ProductCatalog">
    <description>Product listing and search</description>
  </module>
</project>
```

## 参考资料
- [Cursor AI Prompts](https://github.com/mergisi/cursor-ai-prompts)
- [Cursor AI 官方网站](https://cursor.sh)
