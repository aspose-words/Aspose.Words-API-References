---
title: Hyphenation.UnregisterDictionary
second_title: Aspose.Words for .NET API 参考
description: Hyphenation 方法. 注销指定语言的连字符字典
type: docs
weight: 50
url: /zh/net/aspose.words/hyphenation/unregisterdictionary/
---
## Hyphenation.UnregisterDictionary method

注销指定语言的连字符字典。

这与注册 Null 字典不同。注销字典会启用指定语言的回调。

```csharp
public static void UnregisterDictionary(string language)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| language | String | 语言名称，例如“en-US”。有关详细信息，请参阅 .NET 文档中的“区域性名称”和 RFC 4646。 |

### 例子

展示如何注册连字符字典。

```csharp
// 连字符字典包含定义字典语言的连字符规则的字符串列表。
// 当文档包含多行文本时，其中的单词可以被拆分并在下一行继续，
// 连字符将在字典的字符串列表中查找该单词的子字符串。
// 如果字典包含子字符串，那么连字符会将单词分成两行
// 通过子字符串并在前半部分添加连字符。
// 将本地文件系统中的字典文件注册到“de-CH”语言环境。
Hyphenation.RegisterDictionary("de-CH", MyDir + "hyph_de_CH.dic");

Assert.True(Hyphenation.IsDictionaryRegistered("de-CH"));

// 打开一个包含区域设置与我们的字典匹配的文本的文档，
// 并将其保存为固定页面保存格式。该文档中的文本将用连字符连接。
Document doc = new Document(MyDir + "German text.docx");

Assert.True(doc.FirstSection.Body.FirstParagraph.Runs.OfType<Run>().All(
    r => r.Font.LocaleId == new CultureInfo("de-CH").LCID));

doc.Save(ArtifactsDir + "Hyphenation.Dictionary.Registered.pdf");

// 取消注册字典后重新加载文档，
// 并将其保存到另一个 PDF，该 PDF 不会包含连字符文本。
Hyphenation.UnregisterDictionary("de-CH");

Assert.False(Hyphenation.IsDictionaryRegistered("de-CH"));

doc = new Document(MyDir + "German text.docx");
doc.Save(ArtifactsDir + "Hyphenation.Dictionary.Unregistered.pdf");
```

### 也可以看看

* class [Hyphenation](../)
* 命名空间 [Aspose.Words](../../hyphenation/)
* 部件 [Aspose.Words](../../../)


