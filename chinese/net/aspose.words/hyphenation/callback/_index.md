---
title: Hyphenation.Callback
second_title: Aspose.Words for .NET API 参考
description: Hyphenation 财产. 获取或设置用于在构建文档的页面布局时请求字典的回调接口 这允许延迟加载字典这在处理多种语言的文档时可能很有用
type: docs
weight: 10
url: /zh/net/aspose.words/hyphenation/callback/
---
## Hyphenation.Callback property

获取或设置用于在构建文档的页面布局时请求字典的回调接口。 这允许延迟加载字典，这在处理多种语言的文档时可能很有用。

```csharp
public static IHyphenationCallback Callback { get; set; }
```

### 例子

显示如何从文件中打开和注册字典。

```csharp
{
    // 设置一个回调来跟踪在连字字典注册期间发生的警告。
    WarningInfoCollection warningInfoCollection = new WarningInfoCollection();
    Hyphenation.WarningCallback = warningInfoCollection;

    // 通过流注册一个英语（美国）断字字典。
    Stream dictionaryStream = new FileStream(MyDir + "hyph_en_US.dic", FileMode.Open);
    Hyphenation.RegisterDictionary("en-US", dictionaryStream);

    Assert.AreEqual(0, warningInfoCollection.Count);

    // 打开具有 Microsoft Word 可能无法在英语机器上连字的语言环境的文档，例如德语。
    Document doc = new Document(MyDir + "German text.docx");

    // 要在保存时为该文档断字，我们需要一个用于“de-CH”语言代码的断字字典。
    // 此回调将处理对该字典的自动请求。
    Hyphenation.Callback = new CustomHyphenationDictionaryRegister();

    // 当我们保存文档时，德语连字符将生效。
    doc.Save(ArtifactsDir + "Hyphenation.RegisterDictionary.pdf");

    // 这个字典包含两个相同的模式，会触发一个警告。
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

* interface [IHyphenationCallback](../../ihyphenationcallback/)
* class [Hyphenation](../)
* 命名空间 [Aspose.Words](../../hyphenation/)
* 部件 [Aspose.Words](../../../)


