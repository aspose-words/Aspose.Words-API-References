---
title: DocumentBuilder.InsertStructuredDocumentTag
linktitle: InsertStructuredDocumentTag
articleTitle: InsertStructuredDocumentTag
second_title: Aspose.Words for .NET
description: 使用 DocumentBuilder 的 InsertStructuredDocumentTag 方法轻松增强您的文档。轻松添加结构化文档标签，实现更清晰的组织！
type: docs
weight: 480
url: /zh/net/aspose.words/documentbuilder/insertstructureddocumenttag/
---
## DocumentBuilder.InsertStructuredDocumentTag method

插入[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/)进入文档。

```csharp
public StructuredDocumentTag InsertStructuredDocumentTag(SdtType type)
```

### 返回值

这[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/)刚刚插入的节点。

## 例子

展示如何简单地插入结构化文档标签。

```csharp
Document doc = new Document(MyDir + "Rendering.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

builder.MoveTo(doc.FirstSection.Body.Paragraphs[3]);
// 请注意，仅允许插入以下 StructuredDocumentTag 类型：
// SdtType.纯文本、SdtType.富文本、SdtType.复选框、SdtType.下拉列表、
// SdtType.ComboBox，SdtType.Picture，SdtType.Date。
// 插入的 StructuredDocumentTag 的标记级别将被自动检测，并取决于插入的位置。
// 添加的 StructuredDocumentTag 将从光标位置继承段落和字体格式。
StructuredDocumentTag sdtPlain = builder.InsertStructuredDocumentTag(SdtType.PlainText);

doc.Save(ArtifactsDir + "StructuredDocumentTag.InsertStructuredDocumentTag.docx");
```

### 也可以看看

* class [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/)
* enum [SdtType](../../../aspose.words.markup/sdttype/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
