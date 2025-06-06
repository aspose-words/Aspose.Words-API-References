---
title: Hyphenation.Callback
linktitle: Callback
articleTitle: Callback
second_title: Aspose.Words для .NET
description: Оптимизируйте макет документа с помощью свойства Hyphenation Callback. Эффективно загружайте словари для многоязычной обработки и улучшайте пользовательский опыт.
type: docs
weight: 10
url: /ru/net/aspose.words/hyphenation/callback/
---
## Hyphenation.Callback property

Возвращает или задает интерфейс обратного вызова, используемый для запроса словарей при построении макета страницы документа. Это позволяет отложить загрузку словарей, что может быть полезно при обработке документов на многих языках.

```csharp
public static IHyphenationCallback Callback { get; set; }
```

## Примеры

Показывает, как открыть и зарегистрировать словарь из файла.

```csharp
public void RegisterDictionary()
{
    // Настройте обратный вызов, который отслеживает предупреждения, возникающие во время регистрации словаря переносов.
    WarningInfoCollection warningInfoCollection = new WarningInfoCollection();
    Hyphenation.WarningCallback = warningInfoCollection;

    // Регистрация английского (США) словаря переносов по потоку.
    Stream dictionaryStream = new FileStream(MyDir + "hyph_en_US.dic", FileMode.Open);
    Hyphenation.RegisterDictionary("en-US", dictionaryStream);

    Assert.AreEqual(0, warningInfoCollection.Count);

    // Откройте документ с локалью, в которой Microsoft Word может не расставлять переносы на англоязычном компьютере, например, на немецком.
    Document doc = new Document(MyDir + "German text.docx");

    // Чтобы расставить переносы в этом документе при сохранении, нам нужен словарь переносов для кода языка "de-CH".
    // Этот обратный вызов обработает автоматический запрос для этого словаря.
    Hyphenation.Callback = new CustomHyphenationDictionaryRegister();

    // При сохранении документа вступят в силу немецкие переносы.
    doc.Save(ArtifactsDir + "Hyphenation.RegisterDictionary.pdf");

    // Этот словарь содержит два одинаковых шаблона, которые вызовут предупреждение.
    Assert.AreEqual(1, warningInfoCollection.Count);
    Assert.AreEqual(WarningType.MinorFormattingLoss, warningInfoCollection[0].WarningType);
    Assert.AreEqual(WarningSource.Layout, warningInfoCollection[0].Source);
    Assert.AreEqual("Hyphenation dictionary contains duplicate patterns. The only first found pattern will be used. " +
                    "Content can be wrapped differently.", warningInfoCollection[0].Description);

}

/// <summary>
/// Связывает языковые коды ISO с именами файлов локальной системы для файлов словаря переносов.
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

* interface [IHyphenationCallback](../../ihyphenationcallback/)
* class [Hyphenation](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
