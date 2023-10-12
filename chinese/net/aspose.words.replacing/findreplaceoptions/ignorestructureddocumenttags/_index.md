---
title: FindReplaceOptions.IgnoreStructuredDocumentTags
second_title: Aspose.Words for .NET API 参考
description: FindReplaceOptions 财产. 获取或设置一个布尔值指示忽略以下内容StructuredDocumentTag. 默认值为错误的.
type: docs
weight: 120
url: /zh/net/aspose.words.replacing/findreplaceoptions/ignorestructureddocumenttags/
---
## FindReplaceOptions.IgnoreStructuredDocumentTags property

获取或设置一个布尔值，指示忽略以下内容[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/). 默认值为`错误的`.

```csharp
public bool IgnoreStructuredDocumentTags { get; set; }
```

### 评论

当此选项设置为`真的`，内容[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) 将被视为简单文本。

否则，[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/)将作为独立的 Story 进行处理，并且将针对每个单独搜索替换模式[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/), 这样如果模式跨越[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/)，则不会对此类模式执行替换 。

### 例子

展示如何忽略替换中的标签内容。

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");

// 本段包含 SDT。
Paragraph p = (Paragraph)doc.FirstSection.Body.GetChild(NodeType.Paragraph, 2, true);
string textToSearch = p.ToString(SaveFormat.Text).Trim();

FindReplaceOptions options = new FindReplaceOptions() { IgnoreStructuredDocumentTags = true };
doc.Range.Replace(textToSearch, "replacement", options);

doc.Save(ArtifactsDir + "StructuredDocumentTag.IgnoreStructuredDocumentTags.docx");
```

### 也可以看看

* class [FindReplaceOptions](../)
* 命名空间 [Aspose.Words.Replacing](../../findreplaceoptions/)
* 部件 [Aspose.Words](../../../)


