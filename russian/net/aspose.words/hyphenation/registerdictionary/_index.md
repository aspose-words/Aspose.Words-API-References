---
title: Hyphenation.RegisterDictionary
second_title: Справочник по API Aspose.Words для .NET
description: Hyphenation метод. Регистрирует и загружает словарь расстановки переносов для указанного языка из потока. Выдает если словарь не может быть прочитан или имеет неверный формат.
type: docs
weight: 40
url: /ru/net/aspose.words/hyphenation/registerdictionary/
---
## RegisterDictionary(string, Stream) {#registerdictionary}

Регистрирует и загружает словарь расстановки переносов для указанного языка из потока. Выдает, если словарь не может быть прочитан или имеет неверный формат.

```csharp
public static void RegisterDictionary(string language, Stream stream)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| language | String | Название языка, например «en-US». Подробности см. в документации .NET для «имени культуры» и RFC 4646. |
| stream | Stream | Поток для файла словаря в формате OpenOffice. |

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

* class [Hyphenation](../)
* пространство имен [Aspose.Words](../../hyphenation/)
* сборка [Aspose.Words](../../../)

---

## RegisterDictionary(string, string) {#registerdictionary_1}

Регистрирует и загружает словарь расстановки переносов для указанного языка из файла. Выдает, если словарь не может быть прочитан или имеет неверный формат.

Этот метод также можно использовать для регистрации нулевого словаря, чтобы предотвратить[`Callback`](../callback/) от повторного вызова для одного и того же языка.

```csharp
public static void RegisterDictionary(string language, string fileName)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| language | String | Название языка, например «en-US». Подробности см. в документации .NET для «имени культуры» и RFC 4646. |
| fileName | String | Путь к файлу словаря в формате Open Office. |

### Примеры

Показывает, как зарегистрировать словарь переносов.

```csharp
// Словарь расстановки переносов содержит список строк, которые определяют правила расстановки переносов для языка словаря.
// Когда документ содержит строки текста, в которых слово можно разделить и продолжить на следующей строке,
// расстановка переносов будет просматривать список строк словаря на наличие подстрок этого слова.
// Если словарь содержит подстроку, то расстановка переносов разделит слово на две строки
// по подстроке и добавляем дефис в первую половину.
// Регистрируем файл словаря из локальной файловой системы в локали "de-CH".
Hyphenation.RegisterDictionary("de-CH", MyDir + "hyph_de_CH.dic");

Assert.True(Hyphenation.IsDictionaryRegistered("de-CH"));

// Открываем документ, содержащий текст с локалью, соответствующей нашему словарю,
// и сохраняем его в формате сохранения с фиксированной страницей. Текст в этом документе будет написан через дефис.
Document doc = new Document(MyDir + "German text.docx");

Assert.True(doc.FirstSection.Body.FirstParagraph.Runs.OfType<Run>().All(
    r => r.Font.LocaleId == new CultureInfo("de-CH").LCID));

doc.Save(ArtifactsDir + "Hyphenation.Dictionary.Registered.pdf");

// Перезагружаем документ после отмены регистрации словаря,
// и сохраните его в другой PDF-файл, в котором не будет текста с переносами.
Hyphenation.UnregisterDictionary("de-CH");

Assert.False(Hyphenation.IsDictionaryRegistered("de-CH"));

doc = new Document(MyDir + "German text.docx");
doc.Save(ArtifactsDir + "Hyphenation.Dictionary.Unregistered.pdf");
```

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

* class [Hyphenation](../)
* пространство имен [Aspose.Words](../../hyphenation/)
* сборка [Aspose.Words](../../../)


