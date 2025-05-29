---
title: Hyphenation.RegisterDictionary
linktitle: RegisterDictionary
articleTitle: RegisterDictionary
second_title: Aspose.Words для .NET
description: Легко улучшайте обработку текста с помощью метода Hyphenation RegisterDictionary. Легко загружайте словари переносов для конкретных языков для достижения оптимальных результатов.
type: docs
weight: 40
url: /ru/net/aspose.words/hyphenation/registerdictionary/
---
## RegisterDictionary(*string, Stream*) {#registerdictionary}

Регистрирует и загружает словарь переносов для указанного языка из потока. Выдает, если словарь не может быть прочитан или имеет недопустимый формат.

```csharp
public static void RegisterDictionary(string language, Stream stream)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| language | String | Название языка, например "en-US". Подробности см. в документации .NET для "названия культуры" и в RFC 4646. |
| stream | Stream | Поток для файла словаря в формате OpenOffice. |

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

* class [Hyphenation](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## RegisterDictionary(*string, string*) {#registerdictionary_1}

Регистрирует и загружает словарь переносов для указанного языка из файла. Выдает, если словарь не может быть прочитан или имеет недопустимый формат.

Этот метод также можно использовать для регистрации словаря Null, чтобы предотвратить[`Callback`](../callback/) от повторного вызова на один и тот же язык.

```csharp
public static void RegisterDictionary(string language, string fileName)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| language | String | Название языка, например "en-US". Подробности см. в документации .NET для "названия культуры" и в RFC 4646. |
| fileName | String | Путь к файлу словаря в формате Open Office. |

## Примеры

Показывает, как зарегистрировать словарь переносов.

```csharp
// Словарь переносов содержит список строк, определяющих правила переносов для языка словаря.
// Когда документ содержит строки текста, в которых слово может быть разделено и продолжено на следующей строке,
// расстановка переносов будет просматривать список строк словаря для подстрок этого слова.
// Если словарь содержит подстроку, то перенос разделит слово на две строки
// на подстроку и добавляем дефис к первой половине.
// Регистрируем файл словаря из локальной файловой системы в локали "de-CH".
Hyphenation.RegisterDictionary("de-CH", MyDir + "hyph_de_CH.dic");

Assert.True(Hyphenation.IsDictionaryRegistered("de-CH"));

// Открываем документ, содержащий текст с локалью, соответствующей локали нашего словаря,
// и сохранить его в формате сохранения с фиксированной страницей. Текст в этом документе будет расставлен переносами.
Document doc = new Document(MyDir + "German text.docx");

Assert.True(doc.FirstSection.Body.FirstParagraph.Runs.OfType<Run>().All(
    r => r.Font.LocaleId == new CultureInfo("de-CH").LCID));

doc.Save(ArtifactsDir + "Hyphenation.Dictionary.Registered.pdf");

// Перезагрузить документ после отмены регистрации словаря,
// и сохраните его в другом PDF-файле, в котором не будет переносов текста.
Hyphenation.UnregisterDictionary("de-CH");

Assert.False(Hyphenation.IsDictionaryRegistered("de-CH"));

doc = new Document(MyDir + "German text.docx");
doc.Save(ArtifactsDir + "Hyphenation.Dictionary.Unregistered.pdf");
```

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

* class [Hyphenation](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
