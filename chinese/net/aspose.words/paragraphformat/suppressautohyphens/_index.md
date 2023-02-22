---
title: ParagraphFormat.SuppressAutoHyphens
second_title: Aspose.Words for .NET API 参考
description: ParagraphFormat 财产. 指定当前段落是否应免除在文档设置中应用 的任何连字符
type: docs
weight: 360
url: /zh/net/aspose.words/paragraphformat/suppressautohyphens/
---
## ParagraphFormat.SuppressAutoHyphens property

指定当前段落是否应免除在文档设置中应用 的任何连字符。

```csharp
public bool SuppressAutoHyphens { get; set; }
```

### 例子

显示如何抑制段落的断字。

```csharp
Hyphenation.RegisterDictionary("de-CH", MyDir + "hyph_de_CH.dic");

Assert.True(Hyphenation.IsDictionaryRegistered("de-CH"));

// 打开一个包含与我们的字典相匹配的语言环境的文本的文档。
// 当我们将此文档保存为固定的页面保存格式时，其文本将带有连字符。
Document doc = new Document(MyDir + "German text.docx");

// 我们可以将“SuppressAutoHyphens”属性设置为“true”来禁用断字
// 对于特定段落，同时为文档的其余部分保持启用状态。
// 此属性的默认值为 "false",
// 这意味着默认情况下每个段落都使用连字符（如果有的话）。
doc.FirstSection.Body.FirstParagraph.ParagraphFormat.SuppressAutoHyphens = suppressAutoHyphens;

doc.Save(ArtifactsDir + "ParagraphFormat.SuppressHyphens.pdf");
```

### 也可以看看

* class [ParagraphFormat](../)
* 命名空间 [Aspose.Words](../../paragraphformat/)
* 部件 [Aspose.Words](../../../)


