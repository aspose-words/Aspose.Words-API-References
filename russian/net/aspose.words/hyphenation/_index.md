---
title: Hyphenation Class
linktitle: Hyphenation
articleTitle: Hyphenation
second_title: Aspose.Words для .NET
description: Aspose.Words.Hyphenation сорт. Предоставляет методы для работы со словарями расстановки переносов. Эти словари предписывают где слова определенного языка могут быть расставлены через дефис на С#.
type: docs
weight: 3150
url: /ru/net/aspose.words/hyphenation/
---
## Hyphenation class

Предоставляет методы для работы со словарями расстановки переносов. Эти словари предписывают, где слова определенного языка могут быть расставлены через дефис.

Чтобы узнать больше, посетите[Работа с переносами](https://docs.aspose.com/words/net/working-with-hyphenation/) статья документации.

```csharp
public static class Hyphenation
```

## Характеристики

| Имя | Описание |
| --- | --- |
| static [Callback](../../aspose.words/hyphenation/callback/) { get; set; } | Получает или задает интерфейс обратного вызова, используемый для запроса словарей при построении макета страницы документа. Это позволяет задерживать загрузку словарей, что может быть полезно при обработке документов на многих языках. |
| static [WarningCallback](../../aspose.words/hyphenation/warningcallback/) { get; set; } | Вызывается во время загрузки шаблонов расстановки переносов, когда обнаруживается проблема, которая может привести к потере точности форматирования. |

## Методы

| Имя | Описание |
| --- | --- |
| static [IsDictionaryRegistered](../../aspose.words/hyphenation/isdictionaryregistered/)(*string*) | Возвращает`ЛОЖЬ` если для указанного языка не зарегистрирован словарь или зарегистрирован пустой словарь,`истинный` иначе. |
| static [RegisterDictionary](../../aspose.words/hyphenation/registerdictionary/#registerdictionary)(*string, Stream*) | Регистрирует и загружает словарь расстановки переносов для указанного языка из потока. Выдает, если словарь не может быть прочитан или имеет неверный формат. |
| static [RegisterDictionary](../../aspose.words/hyphenation/registerdictionary/#registerdictionary_1)(*string, string*) | Регистрирует и загружает словарь расстановки переносов для указанного языка из файла. Выдает, если словарь не может быть прочитан или имеет неверный формат. |
| static [UnregisterDictionary](../../aspose.words/hyphenation/unregisterdictionary/)(*string*) | Отменяет регистрацию словаря переносов для указанного языка. |

## Примеры

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

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
