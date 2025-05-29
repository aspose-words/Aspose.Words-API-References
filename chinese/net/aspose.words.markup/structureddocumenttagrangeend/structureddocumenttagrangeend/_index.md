---
title: StructuredDocumentTagRangeEnd
linktitle: StructuredDocumentTagRangeEnd
articleTitle: StructuredDocumentTagRangeEnd
second_title: Aspose.Words for .NET
description: 发现 StructuredDocumentTagRangeEnd 构造函数——有效地初始化文档标签范围以增强内容管理和无缝集成。
type: docs
weight: 10
url: /zh/net/aspose.words.markup/structureddocumenttagrangeend/structureddocumenttagrangeend/
---
## StructuredDocumentTagRangeEnd constructor

初始化**结构化文档标签范围结束**类.

```csharp
public StructuredDocumentTagRangeEnd(DocumentBase doc, int id)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| doc | DocumentBase | 所有者文件。 |
| id | Int32 | 相应结构化文档标签范围开始的标识符。 |

## 例子

展示如何创建/删除结构化文档标签及其内容。

```csharp
public void SdtRangeExtendedMethods()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("StructuredDocumentTag element");

    StructuredDocumentTagRangeStart rangeStart = InsertStructuredDocumentTagRanges(doc);

    // 删除范围结构化文档标签，但保留其中的内容。
    rangeStart.RemoveSelfOnly();

    rangeStart = (StructuredDocumentTagRangeStart)doc.GetChild(
        NodeType.StructuredDocumentTagRangeStart, 0, false);
    Assert.AreEqual(null, rangeStart);

    StructuredDocumentTagRangeEnd rangeEnd = (StructuredDocumentTagRangeEnd)doc.GetChild(
        NodeType.StructuredDocumentTagRangeEnd, 0, false);

    Assert.AreEqual(null, rangeEnd);
    Assert.AreEqual("StructuredDocumentTag element", doc.GetText().Trim());

    rangeStart = InsertStructuredDocumentTagRanges(doc);

    Node paragraphNode = rangeStart.LastOrDefault();
    Assert.AreEqual("StructuredDocumentTag element", paragraphNode?.GetText().Trim());

    // 删除范围结构化文档标签及其内部内容。
    rangeStart.RemoveAllChildren();

    paragraphNode = rangeStart.LastOrDefault();
    Assert.AreEqual(null, paragraphNode?.GetText());
}

public StructuredDocumentTagRangeStart InsertStructuredDocumentTagRanges(Document doc)
{
    StructuredDocumentTagRangeStart rangeStart = new StructuredDocumentTagRangeStart(doc, SdtType.PlainText);
    StructuredDocumentTagRangeEnd rangeEnd = new StructuredDocumentTagRangeEnd(doc, rangeStart.Id);

    doc.FirstSection.Body.InsertBefore(rangeStart, doc.FirstSection.Body.FirstParagraph);
    doc.LastSection.Body.InsertAfter(rangeEnd, doc.FirstSection.Body.FirstParagraph);

    return rangeStart;
}
```

### 也可以看看

* class [DocumentBase](../../../aspose.words/documentbase/)
* class [StructuredDocumentTagRangeEnd](../)
* 命名空间 [Aspose.Words.Markup](../../../aspose.words.markup/)
* 部件 [Aspose.Words](../../../)
