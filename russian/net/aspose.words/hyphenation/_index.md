---
title: Hyphenation Class
linktitle: Hyphenation
articleTitle: Hyphenation
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Hyphenation для эффективного управления переносами. Улучшите свои документы с помощью точных правил переносов, специфичных для конкретного языка.
type: docs
weight: 3580
url: /ru/net/aspose.words/hyphenation/
---
## Hyphenation class

Предоставляет методы для работы со словарями переносов. Эти словари предписывают, где слова определенного языка могут переноситься.

Чтобы узнать больше, посетите[Работа с переносами](https://docs.aspose.com/words/net/working-with-hyphenation/) документальная статья.

```csharp
public static class Hyphenation
```

## Характеристики

| Имя | Описание |
| --- | --- |
| static [Callback](../../aspose.words/hyphenation/callback/) { get; set; } | Возвращает или задает интерфейс обратного вызова, используемый для запроса словарей при построении макета страницы документа. Это позволяет отложить загрузку словарей, что может быть полезно при обработке документов на многих языках. |
| static [WarningCallback](../../aspose.words/hyphenation/warningcallback/) { get; set; } | Вызывается во время загрузки шаблонов переносов, когда обнаружена проблема, которая может привести к потере точности форматирования. |

## Методы

| Имя | Описание |
| --- | --- |
| static [IsDictionaryRegistered](../../aspose.words/hyphenation/isdictionaryregistered/)(*string*) | Возврат`ЛОЖЬ` если для указанного языка не зарегистрировано ни одного словаря или зарегистрирован нулевой словарь,`истинный` в противном случае. |
| static [RegisterDictionary](../../aspose.words/hyphenation/registerdictionary/#registerdictionary)(*string, Stream*) | Регистрирует и загружает словарь переносов для указанного языка из потока. Выдает, если словарь не может быть прочитан или имеет недопустимый формат. |
| static [RegisterDictionary](../../aspose.words/hyphenation/registerdictionary/#registerdictionary_1)(*string, string*) | Регистрирует и загружает словарь переносов для указанного языка из файла. Выдает, если словарь не может быть прочитан или имеет недопустимый формат. |
| static [UnregisterDictionary](../../aspose.words/hyphenation/unregisterdictionary/)(*string*) | Отменяет регистрацию словаря переносов для указанного языка. |

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

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
