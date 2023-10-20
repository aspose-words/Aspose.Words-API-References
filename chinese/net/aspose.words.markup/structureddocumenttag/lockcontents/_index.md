---
title: StructuredDocumentTag.LockContents
linktitle: LockContents
articleTitle: LockContents
second_title: 用于 .NET 的 Aspose.Words
description: StructuredDocumentTag LockContents 财产. 当设置为 true 时此属性将禁止用户编辑此内容SDT 在 C#.
type: docs
weight: 200
url: /zh/net/aspose.words.markup/structureddocumenttag/lockcontents/
---
## StructuredDocumentTag.LockContents property

当设置为 true 时，此属性将禁止用户编辑此内容**SDT**.

```csharp
public bool LockContents { get; set; }
```

## 例子

展示如何将编辑限制应用于结构化文档标签。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入纯文本结构化文档标签，作为提示用户填写的文本框。
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// 将“LockContents”属性设置为“true”以禁止用户编辑此文本框的内容。
tag.LockContents = true;
builder.Write("The contents of this structured document tag cannot be edited: ");
builder.InsertNode(tag);

tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// 将“LockContentControl”属性设置为“true”以禁止用户
// 在 Microsoft Word 中手动删除此结构化文档标记。
tag.LockContentControl = true;

builder.InsertParagraph();
builder.Write("This structured document tag cannot be deleted but its contents can be edited: ");
builder.InsertNode(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.Lock.docx");
```

### 也可以看看

* class [StructuredDocumentTag](../)
* 命名空间 [Aspose.Words.Markup](../../../aspose.words.markup/)
* 部件 [Aspose.Words](../../../)
