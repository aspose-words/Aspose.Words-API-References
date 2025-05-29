---
title: Document.RevisionsView
linktitle: RevisionsView
articleTitle: RevisionsView
second_title: Aspose.Words for .NET
description: 轻松管理文档修订！选择原始版本或更新版本，实现无缝协作，提升工作效率。
type: docs
weight: 380
url: /zh/net/aspose.words/document/revisionsview/
---
## Document.RevisionsView property

获取或设置一个值，指示是否使用文档的原始版本或修订版本。

```csharp
public RevisionsView RevisionsView { get; set; }
```

## 评论

默认值为.

## 例子

展示如何在文档的修订视图和原始视图之间切换。

```csharp
Document doc = new Document(MyDir + "Revisions at list levels.docx");
doc.UpdateListLabels();

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;
Assert.AreEqual("1.", paragraphs[0].ListLabel.LabelString);
Assert.AreEqual("a.", paragraphs[1].ListLabel.LabelString);
Assert.AreEqual(string.Empty, paragraphs[2].ListLabel.LabelString);

// 查看文档对象，如同所有修订均已接受。目前支持列表标签。
doc.RevisionsView = RevisionsView.Final;

Assert.AreEqual(string.Empty, paragraphs[0].ListLabel.LabelString);
Assert.AreEqual("1.", paragraphs[1].ListLabel.LabelString);
Assert.AreEqual("a.", paragraphs[2].ListLabel.LabelString);
```

### 也可以看看

* enum [RevisionsView](../../revisionsview/)
* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
