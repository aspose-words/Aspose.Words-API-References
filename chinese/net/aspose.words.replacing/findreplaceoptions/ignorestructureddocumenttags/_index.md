---
title: FindReplaceOptions.IgnoreStructuredDocumentTags
linktitle: IgnoreStructuredDocumentTags
articleTitle: IgnoreStructuredDocumentTags
second_title: Aspose.Words for .NET
description: 探索 FindReplaceOptions 的 IgnoreStructuredDocumentTags 属性。使用此易于使用的布尔设置，控制是否忽略 StructuredDocumentTag 内容。
type: docs
weight: 120
url: /zh/net/aspose.words.replacing/findreplaceoptions/ignorestructureddocumenttags/
---
## FindReplaceOptions.IgnoreStructuredDocumentTags property

获取或设置一个布尔值，指示忽略的内容[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/). 默认值为`错误的`.

```csharp
public bool IgnoreStructuredDocumentTags { get; set; }
```

## 评论

当此选项设置为`真的`，内容[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) 将被视为简单文本。

否则，[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/)将被处理为独立的 Story ，并且将分别搜索每个替换模式[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/), 因此，如果模式跨越[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/)，则不会对此类模式执行替换。

## 例子

展示如何忽略替换标签的内容。

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");

// 本段包含SDT。
Paragraph p = (Paragraph)doc.FirstSection.Body.GetChild(NodeType.Paragraph, 2, true);
string textToSearch = p.ToString(SaveFormat.Text).Trim();

FindReplaceOptions options = new FindReplaceOptions() { IgnoreStructuredDocumentTags = true };
doc.Range.Replace(textToSearch, "replacement", options);

doc.Save(ArtifactsDir + "StructuredDocumentTag.IgnoreStructuredDocumentTags.docx");
```

### 也可以看看

* class [FindReplaceOptions](../)
* 命名空间 [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* 部件 [Aspose.Words](../../../)
