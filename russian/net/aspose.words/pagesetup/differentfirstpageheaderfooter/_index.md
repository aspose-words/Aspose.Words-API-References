---
title: PageSetup.DifferentFirstPageHeaderFooter
linktitle: DifferentFirstPageHeaderFooter
articleTitle: DifferentFirstPageHeaderFooter
second_title: Aspose.Words для .NET
description: Откройте для себя свойство PageSetup DifferentFirstPageHeaderFooter, чтобы настроить первую страницу документа с помощью уникальных верхних и нижних колонтитулов для придания ему профессионального вида.
type: docs
weight: 110
url: /ru/net/aspose.words/pagesetup/differentfirstpageheaderfooter/
---
## PageSetup.DifferentFirstPageHeaderFooter property

True, если на первой странице используется другой верхний или нижний колонтитул.

```csharp
public bool DifferentFirstPageHeaderFooter { get; set; }
```

## Примеры

Показывает, как создавать верхние и нижние колонтитулы в документе с помощью DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Укажите, что нам нужны разные верхние и нижние колонтитулы для первой, четной и нечетной страниц.
builder.PageSetup.DifferentFirstPageHeaderFooter = true;
builder.PageSetup.OddAndEvenPagesHeaderFooter = true;

// Создаем заголовки, затем добавляем в документ три страницы для отображения каждого типа заголовков.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderFirst);
builder.Write("Header for the first page");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderEven);
builder.Write("Header for even pages");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("Header for all other pages");

builder.MoveToSection(0);
builder.Writeln("Page1");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page2");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page3");

doc.Save(ArtifactsDir + "DocumentBuilder.HeadersAndFooters.docx");
```

Показывает, как включить или отключить основные верхние и нижние колонтитулы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ниже приведены два типа верхних/нижних колонтитулов.
// 1 - «Первый» верхний/нижний колонтитул, который отображается на первой странице раздела.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderFirst);
builder.Writeln("First page header.");

builder.MoveToHeaderFooter(HeaderFooterType.FooterFirst);
builder.Writeln("First page footer.");

// 2 — «Основной» верхний/нижний колонтитул, который отображается на каждой странице раздела.
// Мы можем переопределить основной верхний/нижний колонтитул первой и четной страницы.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Writeln("Primary header.");

builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Writeln("Primary footer.");

builder.MoveToSection(0);
builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

// Каждый раздел имеет объект "PageSetup", который определяет свойства, связанные с внешним видом страницы
// такие как ориентация, размер и границы.
// Установите свойство «DifferentFirstPageHeaderFooter» в значение «true», чтобы применить первый верхний/нижний колонтитул к первой странице.
// Установите свойство "DifferentFirstPageHeaderFooter" в значение "false"
// чтобы на первой странице отображался основной верхний/нижний колонтитул.
builder.PageSetup.DifferentFirstPageHeaderFooter = differentFirstPageHeaderFooter;

doc.Save(ArtifactsDir + "PageSetup.DifferentFirstPageHeaderFooter.docx");
```

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

* class [PageSetup](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
