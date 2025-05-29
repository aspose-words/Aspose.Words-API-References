---
title: ParagraphFormat.SuppressAutoHyphens
linktitle: SuppressAutoHyphens
articleTitle: SuppressAutoHyphens
second_title: Aspose.Words for .NET
description: 使用 ParagraphFormat SuppressAutoHyphens 属性控制文档中的连字符，确保段落格式清晰、专业。
type: docs
weight: 380
url: /zh/net/aspose.words/paragraphformat/suppressautohyphens/
---
## ParagraphFormat.SuppressAutoHyphens property

指定当前段落是否应免除文档设置中应用的任何连字符。

```csharp
public bool SuppressAutoHyphens { get; set; }
```

## 例子

展示如何抑制段落的连字符。

```csharp
Hyphenation.RegisterDictionary("de-CH", MyDir + "hyph_de_CH.dic");

Assert.True(Hyphenation.IsDictionaryRegistered("de-CH"));

// 打开一个包含与我们的字典相匹配的语言环境的文本的文档。
// 当我们将此文档保存为固定页面保存格式时，其文本将带有连字符。
Document doc = new Document(MyDir + "German text.docx");

// 我们可以将“SuppressAutoHyphens”属性设置为“true”以禁用连字符
// 针对特定段落，同时保持其对文档的其余部分可用。
// 此属性的默认值为“false”，
// 这意味着每个段落默认使用连字符（如果有）。
doc.FirstSection.Body.FirstParagraph.ParagraphFormat.SuppressAutoHyphens = suppressAutoHyphens;

doc.Save(ArtifactsDir + "ParagraphFormat.SuppressHyphens.pdf");
```

### 也可以看看

* class [ParagraphFormat](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
