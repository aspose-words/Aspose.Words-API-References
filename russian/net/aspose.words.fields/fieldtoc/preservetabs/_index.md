---
title: FieldToc.PreserveTabs
linktitle: PreserveTabs
articleTitle: PreserveTabs
second_title: Aspose.Words для .NET
description: Узнайте, как свойство FieldToc PreserveTabs улучшает управление данными, сохраняя записи вкладок в записях таблиц для лучшей организации.
type: docs
weight: 140
url: /ru/net/aspose.words.fields/fieldtoc/preservetabs/
---
## FieldToc.PreserveTabs property

Возвращает или задает, следует ли сохранять записи табуляции в записях таблицы.

```csharp
public bool PreserveTabs { get; set; }
```

## Примеры

Показывает, как вставить оглавление и заполнить его записями на основе стилей заголовков.

```csharp
public void FieldToc()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.StartBookmark("MyBookmark");

    // Вставьте поле TOC, которое объединит все заголовки в оглавление.
    // Для каждого заголовка это поле создаст строку с текстом в этом стиле заголовка слева,
    // и страница, на которой заголовок отображается справа.
    FieldToc field = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

    // Используйте свойство BookmarkName только для перечисления заголовков
    // которые появляются в пределах закладки с именем «MyBookmark».
    field.BookmarkName = "MyBookmark";

    // Текст со встроенным стилем заголовка, например «Заголовок 1», примененным к нему, будет считаться заголовком.
    // В этом свойстве мы можем указать дополнительные стили, которые будут использоваться в качестве заголовков оглавлением, а также их уровни оглавления.
    field.CustomStyles = "Quote; 6; Intense Quote; 7";

    // По умолчанию уровни стилей/TOC разделяются в свойстве CustomStyles запятой,
    // но мы можем установить пользовательский разделитель в этом свойстве.
    doc.FieldOptions.CustomTocStyleSeparator = ";";

    // Настройте поле, чтобы исключить все заголовки, уровни TOC которых выходят за пределы этого диапазона.
    field.HeadingLevelRange = "1-3";

    // TOC не будет отображать номера страниц заголовков, уровни TOC которых находятся в этом диапазоне.
    field.PageNumberOmittingLevelRange = "2-5";

     // Задайте пользовательскую строку, которая будет отделять каждый заголовок от номера страницы.
    field.EntrySeparator = "-";
    field.InsertHyperlinks = true;
    field.HideInWebLayout = false;
    field.PreserveLineBreaks = true;
    field.PreserveTabs = true;
    field.UseParagraphOutlineLevel = false;

    InsertNewPageWithHeading(builder, "First entry", "Heading 1");
    builder.Writeln("Paragraph text.");
    InsertNewPageWithHeading(builder, "Second entry", "Heading 1");
    InsertNewPageWithHeading(builder, "Third entry", "Quote");
    InsertNewPageWithHeading(builder, "Fourth entry", "Intense Quote");

    // В этих двух заголовках номера страниц будут опущены, поскольку они находятся в диапазоне «2-5».
    InsertNewPageWithHeading(builder, "Fifth entry", "Heading 2");
    InsertNewPageWithHeading(builder, "Sixth entry", "Heading 3");

    // Эта запись не отображается, поскольку «Заголовок 4» находится за пределами диапазона «1-3», который мы установили ранее.
    InsertNewPageWithHeading(builder, "Seventh entry", "Heading 4");

    builder.EndBookmark("MyBookmark");
    builder.Writeln("Paragraph text.");

    // Эта запись не отображается, поскольку она находится за пределами закладки, указанной в оглавлении.
    InsertNewPageWithHeading(builder, "Eighth entry", "Heading 1");

    Assert.AreEqual(" TOC  \\b MyBookmark \\t \"Quote; 6; Intense Quote; 7\" \\o 1-3 \\n 2-5 \\p - \\h \\x \\w", field.GetFieldCode());

    field.UpdatePageNumbers();
    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.TOC.docx");
}

/// <summary>
/// Начать новую страницу и вставить абзац указанного стиля.
/// </summary>
public void InsertNewPageWithHeading(DocumentBuilder builder, string captionText, string styleName)
{
    builder.InsertBreak(BreakType.PageBreak);
    string originalStyle = builder.ParagraphFormat.StyleName;
    builder.ParagraphFormat.Style = builder.Document.Styles[styleName];
    builder.Writeln(captionText);
    builder.ParagraphFormat.Style = builder.Document.Styles[originalStyle];
}
```

### Смотрите также

* class [FieldToc](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
