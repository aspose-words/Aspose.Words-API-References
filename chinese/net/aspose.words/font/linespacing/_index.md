---
title: Font.LineSpacing
linktitle: LineSpacing
articleTitle: LineSpacing
second_title: 用于 .NET 的 Aspose.Words
description: Font LineSpacing 财产. 返回此字体的行距以磅为单位 在 C#.
type: docs
weight: 190
url: /zh/net/aspose.words/font/linespacing/
---
## Font.LineSpacing property

返回此字体的行距（以磅为单位）。

```csharp
public double LineSpacing { get; }
```

## 例子

演示如何获取字体的行距（以磅为单位）。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 为 DocumentBuilder 设置不同的字体并验证它们的行距。
builder.Font.Name = "Calibri";
Assert.AreEqual(14.6484375d, builder.Font.LineSpacing);

builder.Font.Name = "Times New Roman";
Assert.AreEqual(13.798828125d, builder.Font.LineSpacing);
```

### 也可以看看

* class [Font](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
