---
title: Enum RevisionsView
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.RevisionsView 枚举. 允许指定是使用文档的原始版本还是修订版本
type: docs
weight: 4810
url: /zh/net/aspose.words/revisionsview/
---
## RevisionsView enumeration

允许指定是使用文档的原始版本还是修订版本。

```csharp
public enum RevisionsView
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Original | `0` | 指定文档的原始版本。 |
| Final | `1` | 指定文档的修订版本。 |

### 例子

演示如何在文档的修订视图和原始视图之间切换。

```csharp
Document doc = new Document(MyDir + "Revisions at list levels.docx");
doc.UpdateListLabels();

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;
Assert.AreEqual("1.", paragraphs[0].ListLabel.LabelString);
Assert.AreEqual("a.", paragraphs[1].ListLabel.LabelString);
Assert.AreEqual(string.Empty, paragraphs[2].ListLabel.LabelString);

// 查看文档对象，就好像所有修订都被接受一样。目前支持列表标签。
doc.RevisionsView = RevisionsView.Final;

Assert.AreEqual(string.Empty, paragraphs[0].ListLabel.LabelString);
Assert.AreEqual("1.", paragraphs[1].ListLabel.LabelString);
Assert.AreEqual("a.", paragraphs[2].ListLabel.LabelString);
```

### 也可以看看

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)


