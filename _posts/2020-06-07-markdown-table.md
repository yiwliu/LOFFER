---
layout: post 
title: Markdown表格语法
date: 2020-06-07
Author: Sesame
tags: [markdown, grammar]
comments: true 
---

## 表格语法以及展示效果

在进行markdown文件编辑的时候难免需要进行表格的创建，本文将简要介绍如何使用markdown语法创建简单表格。
<!-- more -->

### 语法
使用markdown创建表格的语法如下图所示：
```
title1 | title2 | title3 | title4 
-      | :-     | -:     | :-: 
banana | $1 | 5 | 100
apple | $2 | 10 | 50 
strawberry | $5 | 20 | 999
```
### 效果

title1 | title2 | title3 | title4 
-      | :-     | -:     | :-: 
banana | $1 | 5 | 100
apple | $2 | 10 | 50 
strawberry | $5 | 20 | 999

## 语法解释 
1. 表格第二行 `:-`, `-:`, `:-:` 分别表示内容和标题栏左对齐，右对齐，居中。
2. 内容和｜之间的多余空格忽略。
3. 默认情况（-）下，标题栏和内容居左对齐。
