---
title: Hyphenation.IsDictionaryRegistered
linktitle: IsDictionaryRegistered
articleTitle: IsDictionaryRegistered
second_title: Aspose.Words for .NET
description: 发现 Hyphenation IsDictionaryRegistered 方法，检查是否为您的语言注册了字典，确保您的应用程序中连字符的准确性。
type: docs
weight: 30
url: /zh/net/aspose.words/hyphenation/isdictionaryregistered/
---
## Hyphenation.IsDictionaryRegistered method

返回`错误的`如果对于指定的语言没有注册词典，或者注册的词典为空，`真的`否则。

```csharp
public static bool IsDictionaryRegistered(string language)
```

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
