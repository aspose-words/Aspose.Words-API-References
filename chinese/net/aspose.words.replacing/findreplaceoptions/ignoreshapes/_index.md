---
title: FindReplaceOptions.IgnoreShapes
linktitle: IgnoreShapes
articleTitle: IgnoreShapes
second_title: Aspose.Words for .NET
description: 探索 FindReplaceOptions 的 IgnoreShapes 属性。使用此基本布尔设置控制文本处理中形状的包含，以提高准确性。
type: docs
weight: 110
url: /zh/net/aspose.words.replacing/findreplaceoptions/ignoreshapes/
---
## FindReplaceOptions.IgnoreShapes property

获取或设置一个布尔值，指示是否忽略文本中的形状。

默认值为`错误的`。

```csharp
public bool IgnoreShapes { get; set; }
```

## 例子

展示如何在替换文本时忽略形状。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder.InsertShape(ShapeType.Balloon, 200, 200);
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

FindReplaceOptions findReplaceOptions = new FindReplaceOptions() { IgnoreShapes = true };
builder.Document.Range.Replace("Lorem ipsum dolor sit amet, consectetur adipiscing elit.Lorem ipsum dolor sit amet, consectetur adipiscing elit.",
    "Lorem ipsum dolor sit amet, consectetur adipiscing elit.", findReplaceOptions);
Assert.AreEqual("Lorem ipsum dolor sit amet, consectetur adipiscing elit.", builder.Document.GetText().Trim());
```

### 也可以看看

* class [FindReplaceOptions](../)
* 命名空间 [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* 部件 [Aspose.Words](../../../)
