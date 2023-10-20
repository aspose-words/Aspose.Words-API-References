---
title: Hyphenation Class
linktitle: Hyphenation
articleTitle: Hyphenation
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Hyphenation 班级. 提供使用连字符字典的方法这些词典规定了特定语言的单词可以用连字符连接的位置 在 C#.
type: docs
weight: 3150
url: /zh/net/aspose.words/hyphenation/
---
## Hyphenation class

提供使用连字符字典的方法。这些词典规定了特定语言的单词可以用连字符连接的位置。

要了解更多信息，请访问[使用连字符](https://docs.aspose.com/words/net/working-with-hyphenation/)文档文章。

```csharp
public static class Hyphenation
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| static [Callback](../../aspose.words/hyphenation/callback/) { get; set; } | 获取或设置用于在构建文档页面布局时请求字典的回调接口。 这允许延迟加载字典，这在处理多种语言的文档时可能很有用。 |
| static [WarningCallback](../../aspose.words/hyphenation/warningcallback/) { get; set; } | 在加载连字模式期间，当检测到可能导致格式保真度损失的问题时调用。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| static [IsDictionaryRegistered](../../aspose.words/hyphenation/isdictionaryregistered/)(*string*) | 返回`错误的`如果对于指定的语言没有注册词典或者如果注册的是空词典，`真的`否则. |
| static [RegisterDictionary](../../aspose.words/hyphenation/registerdictionary/#registerdictionary)(*string, Stream*) | 从流中注册并加载指定语言的连字符字典。如果字典无法读取或格式无效，则抛出异常。 |
| static [RegisterDictionary](../../aspose.words/hyphenation/registerdictionary/#registerdictionary_1)(*string, string*) | 从文件中注册并加载指定语言的连字符字典。如果字典无法读取或格式无效，则抛出异常。 |
| static [UnregisterDictionary](../../aspose.words/hyphenation/unregisterdictionary/)(*string*) | 注销指定语言的连字符字典。 |

## 例子

演示如何从文件打开和注册字典。

```csharp
public void RegisterDictionary()
{
    // 设置一个回调来跟踪连字符字典注册期间发生的警告。
    WarningInfoCollection warningInfoCollection = new WarningInfoCollection();
    Hyphenation.WarningCallback = warningInfoCollection;

    // 通过流注册英语（美国）连字符字典。
    Stream dictionaryStream = new FileStream(MyDir + "hyph_en_US.dic", FileMode.Open);
    Hyphenation.RegisterDictionary("en-US", dictionaryStream);

    Assert.AreEqual(0, warningInfoCollection.Count);

    // 打开 Microsoft Word 可能无法在英语机器上连字符的区域设置的文档，例如德语。
    Document doc = new Document(MyDir + "German text.docx");

    // 要在保存时对该文档进行连字符，我们需要一个用于“de-CH”语言代码的连字符字典。
    // 此回调将处理对该字典的自动请求。
    Hyphenation.Callback = new CustomHyphenationDictionaryRegister();

    // 当我们保存文档时，德语连字符将生效。
    doc.Save(ArtifactsDir + "Hyphenation.RegisterDictionary.pdf");

    // 该字典包含两个相同的模式，这将触发警告。
    Assert.AreEqual(1, warningInfoCollection.Count);
    Assert.AreEqual(WarningType.MinorFormattingLoss, warningInfoCollection[0].WarningType);
    Assert.AreEqual(WarningSource.Layout, warningInfoCollection[0].Source);
    Assert.AreEqual("Hyphenation dictionary contains duplicate patterns. The only first found pattern will be used. " +
                    "Content can be wrapped differently.", warningInfoCollection[0].Description);
}

/// <summary>
/// 将 ISO 语言代码与连字符字典文件的本地系统文件名相关联。
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

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
