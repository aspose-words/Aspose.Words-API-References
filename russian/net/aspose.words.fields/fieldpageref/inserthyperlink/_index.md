---
title: FieldPageRef.InsertHyperlink
linktitle: InsertHyperlink
articleTitle: InsertHyperlink
second_title: Aspose.Words для .NET
description: Узнайте, как свойство FieldPageRef InsertHyperlink улучшает ваши документы, легко связывая их с добавленными в закладки абзацами для удобной навигации.
type: docs
weight: 30
url: /ru/net/aspose.words.fields/fieldpageref/inserthyperlink/
---
## FieldPageRef.InsertHyperlink property

Возвращает или задает, следует ли вставлять гиперссылку на отмеченный закладкой абзац.

```csharp
public bool InsertHyperlink { get; set; }
```

## Примеры

Показывает, как вставить поля PAGEREF для отображения относительного расположения закладок.

```csharp
public void FieldPageRef()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    InsertAndNameBookmark(builder, "MyBookmark1");

    // Вставьте поле PAGEREF, отображающее страницу, на которой находится закладка.
    // Установите флаг InsertHyperlink, чтобы поле также функционировало как кликабельная ссылка на закладку.
    Assert.AreEqual(" PAGEREF  MyBookmark3 \\h", 
        InsertFieldPageRef(builder, "MyBookmark3", true, false, "Hyperlink to Bookmark3, on page: ").GetFieldCode());

    // Мы можем использовать флаг \p, чтобы отобразить поле PAGEREF
    // положение закладки относительно положения поля.
    // Bookmark1 находится на той же странице и над этим полем, поэтому отображаемый результат этого поля будет «выше».
    Assert.AreEqual(" PAGEREF  MyBookmark1 \\h \\p", 
        InsertFieldPageRef(builder, "MyBookmark1", true, true, "Bookmark1 is ").GetFieldCode());

    // Bookmark2 будет на той же странице и под этим полем, поэтому отображаемый результат этого поля будет «ниже».
    Assert.AreEqual(" PAGEREF  MyBookmark2 \\h \\p", 
        InsertFieldPageRef(builder, "MyBookmark2", true, true, "Bookmark2 is ").GetFieldCode());

    // Закладка3 будет на другой странице, поэтому поле будет отображаться «на странице 2».
    Assert.AreEqual(" PAGEREF  MyBookmark3 \\h \\p", 
        InsertFieldPageRef(builder, "MyBookmark3", true, true, "Bookmark3 is ").GetFieldCode());

    InsertAndNameBookmark(builder, "MyBookmark2");
    builder.InsertBreak(BreakType.PageBreak);
    InsertAndNameBookmark(builder, "MyBookmark3");

    doc.UpdatePageLayout();
    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.PAGEREF.docx");
}

/// <summary>
/// Использует конструктор документов для вставки поля PAGEREF и задает его свойства.
/// </summary>
private static FieldPageRef InsertFieldPageRef(DocumentBuilder builder, string bookmarkName, bool insertHyperlink, bool insertRelativePosition, string textBefore)
{
    builder.Write(textBefore);

    FieldPageRef field = (FieldPageRef)builder.InsertField(FieldType.FieldPageRef, true);
    field.BookmarkName = bookmarkName;
    field.InsertHyperlink = insertHyperlink;
    field.InsertRelativePosition = insertRelativePosition;
    builder.Writeln();

    return field;
}

/// <summary>
/// Использует конструктор документов для вставки именованной закладки.
/// </summary>
private static void InsertAndNameBookmark(DocumentBuilder builder, string bookmarkName)
{
    builder.StartBookmark(bookmarkName);
    builder.Writeln($"Contents of bookmark \"{bookmarkName}\".");
    builder.EndBookmark(bookmarkName);
}
```

### Смотрите также

* class [FieldPageRef](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
