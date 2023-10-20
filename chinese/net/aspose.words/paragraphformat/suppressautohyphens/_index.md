---
title: ParagraphFormat.SuppressAutoHyphens
linktitle: SuppressAutoHyphens
articleTitle: SuppressAutoHyphens
second_title: 用于 .NET 的 Aspose.Words
description: ParagraphFormat SuppressAutoHyphens 财产. 指定当前段落是否应免除在文档设置中应用的任何连字符  在 C#.
type: docs
weight: 370
url: /zh/net/aspose.words/paragraphformat/suppressautohyphens/
---
## ParagraphFormat.SuppressAutoHyphens property

指定当前段落是否应免除在文档设置中应用的任何连字符。 。

```csharp
public bool SuppressAutoHyphens { get; set; }
```

## 例子

演示如何取消段落的连字符。

```csharp
Hyphenation.RegisterDictionary("de-CH", MyDir + "hyph_de_CH.dic");

Assert.True(Hyphenation.IsDictionaryRegistered("de-CH"));

// 打开一个包含文本的文档，该文本的区域设置与我们的字典的区域设置相匹配。
// 当我们将此文档保存为固定页面保存格式时，其文本将带有连字符。
Document doc = new Document(MyDir + "German text.docx");

// 我们可以将“SuppressAutoHyphens”属性设置为“true”以禁用连字符
// 对于特定段落，同时对文档的其余部分保持启用状态。
// 该属性的默认值为“false”，
// 这意味着默认情况下每个段落都使用连字符（如果有）。
doc.FirstSection.Body.FirstParagraph.ParagraphFormat.SuppressAutoHyphens = suppressAutoHyphens;

doc.Save(ArtifactsDir + "ParagraphFormat.SuppressHyphens.pdf");
```

### 也可以看看

* class [ParagraphFormat](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
