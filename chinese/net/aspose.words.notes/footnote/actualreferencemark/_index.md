---
title: Footnote.ActualReferenceMark
linktitle: ActualReferenceMark
articleTitle: ActualReferenceMark
second_title: Aspose.Words for .NET
description: 发现脚注 ActualReferenceMark 属性以访问文档中引用标记的精确文本，从而增强清晰度和组织性。
type: docs
weight: 20
url: /zh/net/aspose.words.notes/footnote/actualreferencemark/
---
## Footnote.ActualReferenceMark property

获取此脚注在文档中显示的引用标记的实际文本。

```csharp
public string ActualReferenceMark { get; }
```

## 评论

要初始填充文档所有引用标记的此属性值，或在文档发生可能影响引用标记的更改后更新 值，您必须执行 [`UpdateActualReferenceMarks`](../../../aspose.words/document/updateactualreferencemarks/)方法. 更新字段（[`UpdateFields`](../../../aspose.words/document/updatefields/) ）也可能是获得正确结果所必需的。

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

* class [Footnote](../)
* 命名空间 [Aspose.Words.Notes](../../../aspose.words.notes/)
* 部件 [Aspose.Words](../../../)
