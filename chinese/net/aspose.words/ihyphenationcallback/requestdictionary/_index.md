---
title: IHyphenationCallback.RequestDictionary
second_title: Aspose.Words for .NET API 参考
description: IHyphenationCallback 方法. 通知应用程序未找到指定语言的连字符字典可能需要注册
type: docs
weight: 10
url: /zh/net/aspose.words/ihyphenationcallback/requestdictionary/
---
## IHyphenationCallback.RequestDictionary method

通知应用程序未找到指定语言的连字符字典，可能需要注册。

实现应该找到一个字典并使用[`RegisterDictionary`](../../hyphenation/registerdictionary/)方法。

如果字典对于指定的语言实现不可用，可以选择不再调用相同语言 使用[`RegisterDictionary`](../../hyphenation/registerdictionary/)和`无效的`值.

```csharp
public void RequestDictionary(string language)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| language | String | 语言名称，例如“en-US”。有关详细信息，请参阅 .NET 文档中的“区域性名称”和 RFC 4646。 |

### 评论

此方法抛出的异常将中止页面布局过程的执行。

### 例子

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

* interface [IHyphenationCallback](../)
* 命名空间 [Aspose.Words](../../ihyphenationcallback/)
* 部件 [Aspose.Words](../../../)


