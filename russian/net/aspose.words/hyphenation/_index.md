---
title: Hyphenation
second_title: Справочник по API Aspose.Words для .NET
description: Предоставляет методы для работы со словарями переносов. Эти словари предписывают где слова определенного языка могут быть расставлены через дефис.
type: docs
weight: 2970
url: /ru/net/aspose.words/hyphenation/
---
## Hyphenation class

Предоставляет методы для работы со словарями переносов. Эти словари предписывают, где слова определенного языка могут быть расставлены через дефис.

```csharp
public static class Hyphenation
```

## Характеристики

| Имя | Описание |
| --- | --- |
| static [Callback](../../aspose.words/hyphenation/callback/) { get; set; } | Получает или задает интерфейс обратного вызова, используемый для запроса словарей при построении макета страницы документа. Позволяет отложить загрузку словарей, что может быть полезно при обработке документов на многих языках. |
| static [WarningCallback](../../aspose.words/hyphenation/warningcallback/) { get; set; } | Вызывается во время загрузки шаблонов расстановки переносов, когда обнаруживается проблема, которая может привести к потере точности форматирования. |

## Методы

| Имя | Описание |
| --- | --- |
| static [IsDictionaryRegistered](../../aspose.words/hyphenation/isdictionaryregistered/)(string) | Возвращает False, если для указанного языка не зарегистрирован словарь или зарегистрирован пустой словарь, в противном случае True. |
| static [RegisterDictionary](../../aspose.words/hyphenation/registerdictionary/#registerdictionary)(string, Stream) | Регистрирует и загружает словарь переносов для указанного языка из потока. Выдает, если словарь не может быть прочитан или имеет недопустимый формат. |
| static [RegisterDictionary](../../aspose.words/hyphenation/registerdictionary/#registerdictionary_1)(string, string) | Регистрирует и загружает словарь переносов для указанного языка из файла. Выдает, если словарь не может быть прочитан или имеет недопустимый формат. |
| static [UnregisterDictionary](../../aspose.words/hyphenation/unregisterdictionary/)(string) | Отменяет регистрацию словаря переносов для указанного языка. |

### Примеры

Показывает, как открыть и зарегистрировать словарь из файла.

```csharp
{
    // Настраиваем обратный вызов, который отслеживает предупреждения, возникающие при регистрации словаря переносов.
    WarningInfoCollection warningInfoCollection = new WarningInfoCollection();
    Hyphenation.WarningCallback = warningInfoCollection;

    // Зарегистрировать английский (США) словарь переносов по потоку.
    Stream dictionaryStream = new FileStream(MyDir + "hyph_en_US.dic", FileMode.Open);
    Hyphenation.RegisterDictionary("en-US", dictionaryStream);

    Assert.AreEqual(0, warningInfoCollection.Count);

    // Откройте документ с языковым стандартом, в котором Microsoft Word не может использовать дефис на англоязычном компьютере, например немецком.
    Document doc = new Document(MyDir + "German text.docx");

    // Чтобы расставлять переносы в этом документе при сохранении, нам нужен словарь переносов для языкового кода "de-CH".
    // Этот обратный вызов будет обрабатывать автоматический запрос для этого словаря.
    Hyphenation.Callback = new CustomHyphenationDictionaryRegister();

    // Когда мы сохраним документ, немецкие переносы вступят в силу.
    doc.Save(ArtifactsDir + "Hyphenation.RegisterDictionary.pdf");

    // Этот словарь содержит два одинаковых шаблона, которые вызовут предупреждение.
    Assert.AreEqual(1, warningInfoCollection.Count);
    Assert.AreEqual(WarningType.MinorFormattingLoss, warningInfoCollection[0].WarningType);
    Assert.AreEqual(WarningSource.Layout, warningInfoCollection[0].Source);
    Assert.AreEqual("Hyphenation dictionary contains duplicate patterns. The only first found pattern will be used. " +
                    "Content can be wrapped differently.", warningInfoCollection[0].Description);
}

/// <summary>
/// Связывает языковые коды ISO с именами файлов локальной системы для файлов словарей расстановки переносов.
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

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
