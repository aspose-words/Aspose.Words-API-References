---
title: Field.DisplayResult
linktitle: DisplayResult
articleTitle: DisplayResult
second_title: 用于 .NET 的 Aspose.Words
description: Field DisplayResult 财产. 获取表示显示字段结果的文本 在 C#.
type: docs
weight: 10
url: /zh/net/aspose.words.fields/field/displayresult/
---
## Field.DisplayResult property

获取表示显示字段结果的文本。

```csharp
public string DisplayResult { get; }
```

## 评论

的[`UpdateListLabels`](../../../aspose.words/document/updatelistlabels/)必须调用方法以获得 the 的正确值[`FieldListNum`](../../fieldlistnum/),[`FieldAutoNum`](../../fieldautonum/),[`FieldAutoNumOut`](../../fieldautonumout/)和[`FieldAutoNumLgl`](../../fieldautonumlgl/)字段.

## 例子

演示如何获取字段在文档中显示的真实文本。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("This document was written by ");
FieldAuthor fieldAuthor = (FieldAuthor)builder.InsertField(FieldType.FieldAuthor, true);
fieldAuthor.AuthorName = "John Doe";

// 我们可以使用 DisplayResult 属性来验证确切的文本
// 一个字段将显示在文档中的位置。
Assert.AreEqual(string.Empty, fieldAuthor.DisplayResult);

 // 字段不会实时维护准确的结果值。
// 为了确保我们的字段在任何给定时间显示准确的结果，
// 例如在保存操作之前，我们需要手动更新它们。
fieldAuthor.Update();

Assert.AreEqual("John Doe", fieldAuthor.DisplayResult);

doc.Save(ArtifactsDir + "Field.DisplayResult.docx");
```

### 也可以看看

* class [Field](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
