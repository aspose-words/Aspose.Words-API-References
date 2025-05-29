---
title: FindReplaceOptions
linktitle: FindReplaceOptions
articleTitle: FindReplaceOptions
second_title: Aspose.Words для .NET
description: Откройте для себя конструктор FindReplaceOptions, который позволяет легко инициализировать новый экземпляр с настройками по умолчанию, расширяя функциональность поиска и замены.
type: docs
weight: 10
url: /ru/net/aspose.words.replacing/findreplaceoptions/findreplaceoptions/
---
## FindReplaceOptions() {#constructor}

Инициализирует новый экземпляр класса FindReplaceOptions с настройками по умолчанию.

```csharp
public FindReplaceOptions()
```

## Примеры

Показывает, как распознавать и использовать замены в шаблонах замены.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Jason gave money to Paul.");

Regex regex = new Regex(@"([A-z]+) gave money to ([A-z]+)");

FindReplaceOptions options = new FindReplaceOptions();
options.UseSubstitutions = true;

// Использование устаревшего режима не поддерживает многие расширенные функции, поэтому нам нужно установить его в значение «false».
options.LegacyMode = false;

doc.Range.Replace(regex, @"$2 took money from $1", options);

Assert.AreEqual(doc.GetText(), "Paul took money from Jason.\f");
```

### Смотрите также

* class [FindReplaceOptions](../)
* пространство имен [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* сборка [Aspose.Words](../../../)

---

## FindReplaceOptions(*[FindReplaceDirection](../../findreplacedirection/)*) {#constructor_1}

Инициализирует новый экземпляр класса FindReplaceOptions с указанным направлением.

```csharp
public FindReplaceOptions(FindReplaceDirection direction)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| direction | FindReplaceDirection | Направление операции поиска и замены. |

### Смотрите также

* enum [FindReplaceDirection](../../findreplacedirection/)
* class [FindReplaceOptions](../)
* пространство имен [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* сборка [Aspose.Words](../../../)

---

## FindReplaceOptions(*[IReplacingCallback](../../ireplacingcallback/)*) {#constructor_3}

Инициализирует новый экземпляр класса FindReplaceOptions с указанным заменяющим обратным вызовом.

```csharp
public FindReplaceOptions(IReplacingCallback replacingCallback)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| replacingCallback | IReplacingCallback | Обратный вызов, используемый для замены найденного текста. |

## Примеры

Показывает, как отслеживать порядок, в котором операция замены текста проходит по узлам.

```csharp
public void Order(bool differentFirstPageHeaderFooter)
{
    Document doc = new Document(MyDir + "Header and footer types.docx");

    Section firstPageSection = doc.FirstSection;

    ReplaceLog logger = new ReplaceLog();
    FindReplaceOptions options = new FindReplaceOptions(logger);

    // Использование другого верхнего/нижнего колонтитула для первой страницы повлияет на порядок поиска.
    firstPageSection.PageSetup.DifferentFirstPageHeaderFooter = differentFirstPageHeaderFooter;
    doc.Range.Replace(new Regex("(header|footer)"), "", options);

    if (differentFirstPageHeaderFooter)
        Assert.AreEqual("First header\nFirst footer\nSecond header\nSecond footer\nThird header\nThird footer\n", 
            logger.Text.Replace("\r", ""));
    else
        Assert.AreEqual("Third header\nFirst header\nThird footer\nFirst footer\nSecond header\nSecond footer\n", 
            logger.Text.Replace("\r", ""));
}

/// <summary>
/// Во время операции поиска и замены записывает содержимое каждого узла, содержащего текст, который операция «находит»,
/// в том состоянии, в котором он находился до замены.
/// Это отобразит порядок, в котором операция замены текста проходит по узлам.
/// </summary>
private class ReplaceLog : IReplacingCallback
{
    public ReplaceAction Replacing(ReplacingArgs args)
    {
        mTextBuilder.AppendLine(args.MatchNode.GetText());
        return ReplaceAction.Skip;
    }

    internal string Text => mTextBuilder.ToString();

    private readonly StringBuilder mTextBuilder = new StringBuilder();
}
```

### Смотрите также

* interface [IReplacingCallback](../../ireplacingcallback/)
* class [FindReplaceOptions](../)
* пространство имен [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* сборка [Aspose.Words](../../../)

---

## FindReplaceOptions(*[FindReplaceDirection](../../findreplacedirection/), [IReplacingCallback](../../ireplacingcallback/)*) {#constructor_2}

Инициализирует новый экземпляр класса FindReplaceOptions с указанным направлением и заменяющим обратным вызовом.

```csharp
public FindReplaceOptions(FindReplaceDirection direction, IReplacingCallback replacingCallback)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| direction | FindReplaceDirection | Направление операции поиска и замены. |
| replacingCallback | IReplacingCallback | Обратный вызов, используемый для замены найденного текста. |

### Смотрите также

* enum [FindReplaceDirection](../../findreplacedirection/)
* interface [IReplacingCallback](../../ireplacingcallback/)
* class [FindReplaceOptions](../)
* пространство имен [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* сборка [Aspose.Words](../../../)
