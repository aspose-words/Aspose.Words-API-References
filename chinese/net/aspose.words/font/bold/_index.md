---
title: Font.Bold
linktitle: Bold
articleTitle: Bold
second_title: Aspose.Words for .NET
description: 发现字体粗体属性，轻松识别您的文本是否加粗，增强您的网页设计项目的可读性和风格。
type: docs
weight: 40
url: /zh/net/aspose.words/font/bold/
---
## Font.Bold property

如果字体格式为粗体，则为真。

```csharp
public bool Bold { get; set; }
```

## 例子

展示如何使用 DocumentBuilder 插入格式化文本。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 指定字体格式，然后添加文本。
Aspose.Words.Font font = builder.Font;
font.Size = 16;
font.Bold = true;
font.Color = Color.Blue;
font.Name = "Courier New";
font.Underline = Underline.Dash;

builder.Write("Hello world!");
```

### 也可以看看

* class [Font](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
