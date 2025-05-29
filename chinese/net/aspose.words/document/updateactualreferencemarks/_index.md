---
title: Document.UpdateActualReferenceMarks
linktitle: UpdateActualReferenceMarks
articleTitle: UpdateActualReferenceMarks
second_title: Aspose.Words for .NET
description: 使用 Document UpdateActualReferenceMarks 方法轻松更新文档中的所有脚注和尾注，提高准确性和效率。
type: docs
weight: 800
url: /zh/net/aspose.words/document/updateactualreferencemarks/
---
## Document.UpdateActualReferenceMarks method

更新[`ActualReferenceMark`](../../../aspose.words.notes/footnote/actualreferencemark/)文档中所有脚注和尾注的属性。

```csharp
public void UpdateActualReferenceMarks()
```

## 评论

更新字段（[`UpdateFields`](../updatefields/) ）可能是获得正确结果所必需的。

## 例子

展示如何获取实际的脚注引用标记。

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

Footnote footnote = (Footnote)doc.GetChild(NodeType.Footnote, 1, true);
doc.UpdateFields();
doc.UpdateActualReferenceMarks();

Assert.AreEqual("1", footnote.ActualReferenceMark);
```

### 也可以看看

* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
