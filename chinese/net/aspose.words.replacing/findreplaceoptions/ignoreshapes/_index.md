---
title: FindReplaceOptions.IgnoreShapes
linktitle: IgnoreShapes
articleTitle: IgnoreShapes
second_title: 用于 .NET 的 Aspose.Words
description: FindReplaceOptions IgnoreShapes 财产. 获取或设置一个布尔值指示忽略文本中的形状 在 C#.
type: docs
weight: 110
url: /zh/net/aspose.words.replacing/findreplaceoptions/ignoreshapes/
---
## FindReplaceOptions.IgnoreShapes property

获取或设置一个布尔值，指示忽略文本中的形状。

默认值为`错误的`。

```csharp
public bool IgnoreShapes { get; set; }
```

## 例子

演示如何在替换文本时忽略形状。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder.InsertShape(ShapeType.Balloon, 200, 200);            
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

builder.Document.Range.Replace("Lorem ipsum dolor sit amet, consectetur adipiscing elit.Lorem ipsum dolor sit amet, consectetur adipiscing elit.",
    "Lorem ipsum dolor sit amet, consectetur adipiscing elit.", new FindReplaceOptions() { IgnoreShapes = true });
Assert.AreEqual("Lorem ipsum dolor sit amet, consectetur adipiscing elit.", builder.Document.GetText().Trim());
```

### 也可以看看

* class [FindReplaceOptions](../)
* 命名空间 [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* 部件 [Aspose.Words](../../../)
