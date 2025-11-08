# Yaml syntactic
YAML (YAML Ain't Markup Language) 是一种人类友好的数据序列化格式，常用于配置文件。以下是YAML的基本语法规则：

## 基本语法结构

### 1. 键值对
```yaml
# 基本键值对
name: John Doe
age: 30
city: New York

# 字符串可以加引号（可选）
description: "This is a string"
message: 'Another string'
```

### 2. 列表/数组
```yaml
# 短横线表示列表项
fruits:
  - apple
  - banana
  - orange

# 或者内联写法
numbers: [1, 2, 3, 4, 5]
```

### 3. 嵌套结构
```yaml
person:
  name: Alice
  age: 25
  address:
    street: "123 Main St"
    city: "Boston"
    zip: "02108"
  hobbies:
    - reading
    - swimming
    - coding
```

### 4. 布尔值
```yaml
is_active: true
is_admin: false
debug_mode: on
production: off
```

### 5. 数字
```yaml
integer: 42
float: 3.14
scientific: 1.23e-4
```

### 6. 空值
```yaml
empty_value: null
another_null: ~
```

## 重要语法规则

### 1. 缩进
```yaml
# 使用空格缩进（推荐2个空格）
parent:
  child1: value1
  child2:
    grandchild: value2

# 错误：不能使用Tab
# parent:
# 	child: value  # ❌ 使用Tab
```

### 2. 注释
```yaml
# 这是单行注释
name: John  # 行尾注释

# 多行注释
# 每行都需要#
# 注释符号
```

### 3. 多行字符串
```yaml
# 使用 | 保留换行
description: |
  This is a multi-line
  string that preserves
  line breaks.

# 使用 > 折叠换行
summary: >
  This is a multi-line
  string that gets folded
  into a single line.
```

### 4. 引号的使用
```yaml
# 需要引号的情况
special_chars: "Hello: World"
with_quotes: 'He said "Hello"'
empty_string: ""
number_as_string: "123"

# 不需要引号的情况
simple_string: Hello
no_spaces: HelloWorld
```

## 高级特性

### 1. 锚点和别名
```yaml
defaults: &defaults
  timeout: 30
  retries: 3

production:
  <<: *defaults
  host: prod.example.com

development:
  <<: *defaults
  host: dev.example.com
  timeout: 10
```

### 2. 文档分隔符
```yaml
---
# 第一个文档
app_name: MyApp
version: 1.0

---
# 第二个文档
database:
  host: localhost
  port: 5432
```

### 3. 类型转换
```yaml
# 明确指定类型
date: !!str 2023-12-25
number: !!int "42"
boolean: !!bool "true"
```

## 常见错误

1. **缩进不一致**：混用空格和Tab
2. **冒号后缺少空格**：`key:value` ❌ → `key: value` ✅
3. **特殊字符未加引号**：`text: Hello: World` ❌ → `text: "Hello: World"` ✅
4. **列表项缩进错误**：短横线后必须有空格

YAML的设计目标是简洁易读，特别适合配置文件和数据交换场景。