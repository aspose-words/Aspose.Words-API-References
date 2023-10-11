---
title: Hyphenation.WarningCallback
second_title: Справочник по API Aspose.Words для .NET
description: Hyphenation свойство. Вызывается во время загрузки шаблонов расстановки переносов когда обнаруживается проблема которая может привести к потере точности форматирования.
type: docs
weight: 20
url: /ru/net/aspose.words/hyphenation/warningcallback/
---
## Hyphenation.WarningCallback property

Вызывается во время загрузки шаблонов расстановки переносов, когда обнаруживается проблема, которая может привести к потере точности форматирования.

```csharp
public static IWarningCallback WarningCallback { get; set; }
```

### Примеры

Показывает, как открыть и зарегистрировать словарь из файла.

```csharp
public void RegisterDictionary()
{
    // Настраиваем обратный вызов, который отслеживает предупреждения, возникающие во время регистрации словаря расстановки переносов.
    WarningInfoCollection warningInfoCollection = new WarningInfoCollection();
    Hyphenation.WarningCallback = warningInfoCollection;

    // Регистрируем английский (США) словарь расстановки переносов по потоку.
    Stream dictionaryStream = new FileStream(MyDir + "hyph_en_US.dic", FileMode.Open);
    Hyphenation.RegisterDictionary("en-US", dictionaryStream);

    Assert.AreEqual(0, warningInfoCollection.Count);

    // Откройте документ с языковым стандартом, в котором Microsoft Word не может расставлять переносы на английской машине, например, на немецком.
    Document doc = new Document(MyDir + "German text.docx");

    // Чтобы расставить переносы в этом документе при сохранении, нам нужен словарь расстановки переносов для кода языка "de-CH".
    // Этот обратный вызов будет обрабатывать автоматический запрос этого словаря.
    Hyphenation.Callback = new CustomHyphenationDictionaryRegister();

    // Когда мы сохраним документ, вступят в силу немецкие переносы.
    doc.Save(ArtifactsDir + "Hyphenation.RegisterDictionary.pdf");

    // Этот словарь содержит два одинаковых шаблона, которые вызовут предупреждение.
    Assert.AreEqual(1, warningInfoCollection.Count);
    Assert.AreEqual(WarningType.MinorFormattingLoss, warningInfoCollection[0].WarningType);
    Assert.AreEqual(WarningSource.Layout, warningInfoCollection[0].Source);
    Assert.AreEqual("Hyphenation dictionary contains duplicate patterns. The only first found pattern will be used. " +
                    "Content can be wrapped differently.", warningInfoCollection[0].Description);
}

/// <summary>
/// Связывает языковые коды ISO с именами локальных системных файлов для файлов словаря расстановки переносов.
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

### Смотрите также

* interface [IWarningCallback](../../iwarningcallback/)
* class [Hyphenation](../)
* пространство имен [Aspose.Words](../../hyphenation/)
* сборка [Aspose.Words](../../../)


