---
title: Hyphenation.RegisterDictionary
linktitle: RegisterDictionary
articleTitle: RegisterDictionary
second_title: Aspose.Words for .NET
description: 使用 Hyphenation RegisterDictionary 方法轻松增强文本处理。无缝加载特定语言的连字词典，以获得最佳效果。
type: docs
weight: 40
url: /zh/net/aspose.words/hyphenation/registerdictionary/
---
## RegisterDictionary(*string, Stream*) {#registerdictionary}

从流中注册并加载指定语言的连字词典。如果词典无法读取或格式无效，则抛出异常。

```csharp
public static void RegisterDictionary(string language, Stream stream)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| language | String | 语言名称，例如“en-US”。有关“文化名称”的详细信息，请参阅 .NET 文档以及 RFC 4646。 |
| stream | Stream | OpenOffice 格式的字典文件流。 |

## 例子

展示如何从文件打开和注册字典。

```csharp
public void RegisterDictionary()
{
    // 设置一个回调来跟踪连字字典注册期间发生的警告。
    WarningInfoCollection warningInfoCollection = new WarningInfoCollection();
    Hyphenation.WarningCallback = warningInfoCollection;

    // 通过流注册英语（美国）连字符词典。
    Stream dictionaryStream = new FileStream(MyDir + "hyph_en_US.dic", FileMode.Open);
    Hyphenation.RegisterDictionary("en-US", dictionaryStream);

    Assert.AreEqual(0, warningInfoCollection.Count);

    // 打开一个 Microsoft Word 可能无法在英语机器上使用连字符的语言环境的文档，例如德语。
    Document doc = new Document(MyDir + "German text.docx");

    // 为了在保存时对该文档进行连字，我们需要一个“de-CH”语言代码的连字词典。
    // 此回调将处理该字典的自动请求。
    Hyphenation.Callback = new CustomHyphenationDictionaryRegister();

    // 当我们保存文档时，德语连字符将会生效。
    doc.Save(ArtifactsDir + "Hyphenation.RegisterDictionary.pdf");

    // 此字典包含两个相同的模式，这将触发警告。
    Assert.AreEqual(1, warningInfoCollection.Count);
    Assert.AreEqual(WarningType.MinorFormattingLoss, warningInfoCollection[0].WarningType);
    Assert.AreEqual(WarningSource.Layout, warningInfoCollection[0].Source);
    Assert.AreEqual("Hyphenation dictionary contains duplicate patterns. The only first found pattern will be used. " +
                    "Content can be wrapped differently.", warningInfoCollection[0].Description);

}

/// <summary>
/// 将 ISO 语言代码与连字词典文件的本地系统文件名关联。
/// </summary>
private class CustomHyphenationDictionaryRegister : IHyphenationCallback
{
    public CustomHyphenationDictionaryRegister()
    {
        mHyphenationDictionaryFiles = new Dictionary<string, string>
        {
            { "en-US", MyDir + "hyph_en_US.dic" },
            { "de-CH", MyDir + "hyph_de_CH.dic" }
        };
    }

    public void RequestDictionary(string language)
    {
        Console.Write("Hyphenation dictionary requested: " + language);

        if (Hyphenation.IsDictionaryRegistered(language))
        {
            Console.WriteLine(", is already registered.");
            return;
        }

        if (mHyphenationDictionaryFiles.ContainsKey(language))
        {
            Hyphenation.RegisterDictionary(language, mHyphenationDictionaryFiles[language]);
            Console.WriteLine(", successfully registered.");
            return;
        }

        Console.WriteLine(", no respective dictionary file known by this Callback.");
    }

    private readonly Dictionary<string, string> mHyphenationDictionaryFiles;
}
```

### 也可以看看

* class [Hyphenation](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)

---

## RegisterDictionary(*string, string*) {#registerdictionary_1}

从文件注册并加载指定语言的连字词典。如果词典无法读取或格式无效，则抛出异常。

该方法也可以用于注册空字典，以防止[`Callback`](../callback/)因同一种语言而被反复调用。

```csharp
public static void RegisterDictionary(string language, string fileName)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| language | String | 语言名称，例如“en-US”。有关“文化名称”的详细信息，请参阅 .NET 文档以及 RFC 4646。 |
| fileName | String | Open Office 格式的词典文件的路径。 |

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

展示如何从文件打开和注册字典。

```csharp
public void RegisterDictionary()
{
    // 设置一个回调来跟踪连字字典注册期间发生的警告。
    WarningInfoCollection warningInfoCollection = new WarningInfoCollection();
    Hyphenation.WarningCallback = warningInfoCollection;

    // 通过流注册英语（美国）连字符词典。
    Stream dictionaryStream = new FileStream(MyDir + "hyph_en_US.dic", FileMode.Open);
    Hyphenation.RegisterDictionary("en-US", dictionaryStream);

    Assert.AreEqual(0, warningInfoCollection.Count);

    // 打开一个 Microsoft Word 可能无法在英语机器上使用连字符的语言环境的文档，例如德语。
    Document doc = new Document(MyDir + "German text.docx");

    // 为了在保存时对该文档进行连字，我们需要一个“de-CH”语言代码的连字词典。
    // 此回调将处理该字典的自动请求。
    Hyphenation.Callback = new CustomHyphenationDictionaryRegister();

    // 当我们保存文档时，德语连字符将会生效。
    doc.Save(ArtifactsDir + "Hyphenation.RegisterDictionary.pdf");

    // 此字典包含两个相同的模式，这将触发警告。
    Assert.AreEqual(1, warningInfoCollection.Count);
    Assert.AreEqual(WarningType.MinorFormattingLoss, warningInfoCollection[0].WarningType);
    Assert.AreEqual(WarningSource.Layout, warningInfoCollection[0].Source);
    Assert.AreEqual("Hyphenation dictionary contains duplicate patterns. The only first found pattern will be used. " +
                    "Content can be wrapped differently.", warningInfoCollection[0].Description);

}

/// <summary>
/// 将 ISO 语言代码与连字词典文件的本地系统文件名关联。
/// </summary>
private class CustomHyphenationDictionaryRegister : IHyphenationCallback
{
    public CustomHyphenationDictionaryRegister()
    {
        mHyphenationDictionaryFiles = new Dictionary<string, string>
        {
            { "en-US", MyDir + "hyph_en_US.dic" },
            { "de-CH", MyDir + "hyph_de_CH.dic" }
        };
    }

    public void RequestDictionary(string language)
    {
        Console.Write("Hyphenation dictionary requested: " + language);

        if (Hyphenation.IsDictionaryRegistered(language))
        {
            Console.WriteLine(", is already registered.");
            return;
        }

        if (mHyphenationDictionaryFiles.ContainsKey(language))
        {
            Hyphenation.RegisterDictionary(language, mHyphenationDictionaryFiles[language]);
            Console.WriteLine(", successfully registered.");
            return;
        }

        Console.WriteLine(", no respective dictionary file known by this Callback.");
    }

    private readonly Dictionary<string, string> mHyphenationDictionaryFiles;
}
```

### 也可以看看

* class [Hyphenation](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
