---
title: DocumentBuilder.InsertDocumentInline
linktitle: InsertDocumentInline
articleTitle: InsertDocumentInline
second_title: Aspose.Words for .NET
description: 使用 DocumentBuilder InsertDocumentInline 方法轻松插入文档，增强您的工作流程和文档编辑体验。
type: docs
weight: 320
url: /zh/net/aspose.words/documentbuilder/insertdocumentinline/
---
## DocumentBuilder.InsertDocumentInline method

在光标位置插入内联文档。

```csharp
public Node InsertDocumentInline(Document srcDoc, ImportFormatMode importFormatMode, 
    ImportFormatOptions importFormatOptions)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| srcDoc | Document | 插入的源文档。 |
| importFormatMode | ImportFormatMode | 指定如何合并冲突的样式格式。 |
| importFormatOptions | ImportFormatOptions | 允许指定影响结果文档格式的选项。 |

### 返回值

插入内容的第一个节点。

## 评论

此方法模仿 MS Word 行为，就像按下 CTRL+'A'（选择所有内容）， 然后在某个文档内按下 CTRL+'C'（将选定内容复制到缓冲区）， 然后在另一个文档内按下 CTRL+'V'（从缓冲区插入内容）。

与[`InsertDocument`](../insertdocument/) 此方法将目标文档中插入源文档之前段落的内容移动到插入的源文档的最后一个段落中。实际上，这意味着删除了插入的最后一个段落的段落分隔符。

请注意，如果源文档的最后一个节点不是段落，则不会执行任何操作。

## 例子

显示如何在光标位置插入内联文档。

```csharp
DocumentBuilder srcDoc = new DocumentBuilder();
srcDoc.Write("[src content]");

// 创建目标文档。
DocumentBuilder dstDoc = new DocumentBuilder();
dstDoc.Write("Before ");
dstDoc.InsertNode(new BookmarkStart(dstDoc.Document, "src_place"));
dstDoc.InsertNode(new BookmarkEnd(dstDoc.Document, "src_place"));
dstDoc.Write(" after");

Assert.AreEqual("Before  after", dstDoc.Document.GetText().TrimEnd());

// 将源文档内联插入目标文档。
dstDoc.MoveToBookmark("src_place");
dstDoc.InsertDocumentInline(srcDoc.Document, ImportFormatMode.UseDestinationStyles, new ImportFormatOptions());

Assert.AreEqual("Before [src content] after", dstDoc.Document.GetText().TrimEnd());
```

### 也可以看看

* class [Node](../../node/)
* class [Document](../../document/)
* enum [ImportFormatMode](../../importformatmode/)
* class [ImportFormatOptions](../../importformatoptions/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
