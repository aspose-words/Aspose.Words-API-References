---
title: Hyphenation.UnregisterDictionary
linktitle: UnregisterDictionary
articleTitle: UnregisterDictionary
second_title: Aspose.Words for .NET
description: 使用 UnregisterDictionary 方法轻松删除任何语言的连字符词典，增强文本的清晰度和可读性。
type: docs
weight: 50
url: /zh/net/aspose.words/hyphenation/unregisterdictionary/
---
## Hyphenation.UnregisterDictionary method

取消注册指定语言的连字符词典。

这与注册空字典不同。取消注册字典会启用指定语言的回调。

```csharp
public static void UnregisterDictionary(string language)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| language | String | 语言名称，例如“en-US”。有关“文化名称”的详细信息，请参阅 .NET 文档以及 RFC 4646。 |

## 例子

展示如何注册连字词典。

```csharp
// 连字符字典包含定义字典语言的连字符规则的字符串列表。
// 当文档包含文本行，其中一个单词可以拆分并在下一行继续时，
// 连字符将在字典的字符串列表中查找该单词的子字符串。
// 如果字典包含子字符串，则连字符会将单词分成两行
// 通过子字符串并在前半部分添加连字符。
// 将本地文件系统中的字典文件注册到“de-CH”语言环境。
Hyphenation.RegisterDictionary("de-CH", MyDir + "hyph_de_CH.dic");

Assert.True(Hyphenation.IsDictionaryRegistered("de-CH"));

// 打开一个包含与我们的字典相匹配的语言环境的文本的文档，
// 并将其保存为固定页面保存格式。该文档中的文本将被连字符连接。
Document doc = new Document(MyDir + "German text.docx");

Assert.True(doc.FirstSection.Body.FirstParagraph.Runs.OfType<Run>().All(
    r => r.Font.LocaleId == new CultureInfo("de-CH").LCID));

doc.Save(ArtifactsDir + "Hyphenation.Dictionary.Registered.pdf");

// 取消注册字典后重新加载文档，
// 并将其保存到另一个 PDF，该 PDF 将不包含连字符文本。
Hyphenation.UnregisterDictionary("de-CH");

Assert.False(Hyphenation.IsDictionaryRegistered("de-CH"));

doc = new Document(MyDir + "German text.docx");
doc.Save(ArtifactsDir + "Hyphenation.Dictionary.Unregistered.pdf");
```

### 也可以看看

* class [Hyphenation](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
