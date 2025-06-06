---
title: Field.DisplayResult
linktitle: DisplayResult
articleTitle: DisplayResult
second_title: Aspose.Words for .NET
description: 发现字段 DisplayResult 属性，该属性可提供显示的字段结果的文本，从而增强清晰度和用户体验。
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

[`UpdateListLabels`](../../../aspose.words/document/updatelistlabels/)必须调用方法来获取 the 的正确值[`FieldListNum`](../../fieldlistnum/)，[`FieldAutoNum`](../../fieldautonum/)，[`FieldAutoNumOut`](../../fieldautonumout/)和[`FieldAutoNumLgl`](../../fieldautonumlgl/)字段.

## 例子

展示如何获取文档中字段显示的真实文本。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("This document was written by ");
FieldAuthor fieldAuthor = (FieldAuthor)builder.InsertField(FieldType.FieldAuthor, true);
fieldAuthor.AuthorName = "John Doe";

// 我们可以使用 DisplayResult 属性来验证确切的文本
// 字段将显示在文档中它的位置。
Assert.AreEqual(string.Empty, fieldAuthor.DisplayResult);

 // 字段不能实时维护准确的结果值。
// 为确保我们的字段在任何给定时间显示准确的结果，
// 例如在保存操作之前，我们需要手动更新它们。
fieldAuthor.Update();

Assert.AreEqual("John Doe", fieldAuthor.DisplayResult);

doc.Save(ArtifactsDir + "Field.DisplayResult.docx");
```

### 也可以看看

* class [Field](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
