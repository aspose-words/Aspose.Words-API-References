---
title: IStructuredDocumentTag.LockContentControl
linktitle: LockContentControl
articleTitle: LockContentControl
second_title: Aspose.Words for .NET
description: 发现 IStructuredDocumentTag LockContentControl 属性。设置为 true 可阻止用户删除 SDT，从而增强文档的完整性和控制力。
type: docs
weight: 70
url: /zh/net/aspose.words.markup/istructureddocumenttag/lockcontentcontrol/
---
## IStructuredDocumentTag.LockContentControl property

设置为 true 时，此属性将禁止用户删除此**特殊和差别待遇**.

```csharp
public bool LockContentControl { get; set; }
```

## 例子

展示如何对结构化文档标签应用编辑限制。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入纯文本结构化文档标签，该标签作为文本框，提示用户填写。
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// 将“LockContents”属性设置为“true”以禁止用户编辑此文本框的内容。
tag.LockContents = true;
builder.Write("The contents of this structured document tag cannot be edited: ");
builder.InsertNode(tag);

tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// 将“LockContentControl”属性设置为“true”以禁止用户
// 在 Microsoft Word 中手动删除此结构化文档标签。
tag.LockContentControl = true;

builder.InsertParagraph();
builder.Write("This structured document tag cannot be deleted but its contents can be edited: ");
builder.InsertNode(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.Lock.docx");
```

### 也可以看看

* interface [IStructuredDocumentTag](../)
* 命名空间 [Aspose.Words.Markup](../../../aspose.words.markup/)
* 部件 [Aspose.Words](../../../)
