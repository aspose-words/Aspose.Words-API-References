---
title: Font.Bold
linktitle: Bold
articleTitle: Bold
second_title: 用于 .NET 的 Aspose.Words
description: Font Bold 财产. 如果字体格式为粗体则为真 在 C#.
type: docs
weight: 40
url: /zh/net/aspose.words/font/bold/
---
## Font.Bold property

如果字体格式为粗体则为真。

```csharp
public bool Bold { get; set; }
```

## 例子

演示如何使用 DocumentBuilder 插入格式化文本。

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
