---
title: FieldRef.InsertParagraphNumber
linktitle: InsertParagraphNumber
articleTitle: InsertParagraphNumber
second_title: Aspose.Words для .NET
description: Узнайте, как свойство FieldRef InsertParagraphNumber позволяет вам легко вставлять точные номера абзацев из документа для улучшенного управления ссылками.
type: docs
weight: 50
url: /ru/net/aspose.words.fields/fieldref/insertparagraphnumber/
---
## FieldRef.InsertParagraphNumber property

Возвращает или задает, следует ли вставлять номер абзаца, на который указывает ссылка, точно так же, как он отображается в документе.

```csharp
public bool InsertParagraphNumber { get; set; }
```

## Примеры

Показывает, как вставлять поля REF в закладки ссылок.

```csharp
public void FieldRef()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.StartBookmark("MyBookmark");
    builder.InsertFootnote(FootnoteType.Footnote, "MyBookmark footnote #1");
    builder.Write("Text that will appear in REF field");
    builder.InsertFootnote(FootnoteType.Footnote, "MyBookmark footnote #2");
    builder.EndBookmark("MyBookmark");
    builder.MoveToDocumentStart();

    // Мы применим пользовательский формат списка, в котором количество угловых скобок указывает на текущий уровень списка.
    builder.ListFormat.ApplyNumberDefault();
    builder.ListFormat.ListLevel.NumberFormat = "> \x0000";

    // Вставляем поле REF, которое будет содержать текст в нашей закладке, действовать как гиперссылка и клонировать сноски закладки.
    FieldRef field = InsertFieldRef(builder, "MyBookmark", "", "\n");
    field.IncludeNoteOrComment = true;
    field.InsertHyperlink = true;

    Assert.AreEqual(" REF  MyBookmark \\f \\h", field.GetFieldCode());

    // Вставьте поле REF и отобразите, находится ли указанная закладка выше или ниже него.
    field = InsertFieldRef(builder, "MyBookmark", "The referenced paragraph is ", " this field.\n");
    field.InsertRelativePosition = true;

    Assert.AreEqual(" REF  MyBookmark \\p", field.GetFieldCode());

    // Отображаем номер списка закладки, как он отображается в документе.
    field = InsertFieldRef(builder, "MyBookmark", "The bookmark's paragraph number is ", "\n");
    field.InsertParagraphNumber = true;

    Assert.AreEqual(" REF  MyBookmark \\n", field.GetFieldCode());

    // Отображаем номер списка закладок, но без символов-разделителей, таких как угловые скобки.
    field = InsertFieldRef(builder, "MyBookmark", "The bookmark's paragraph number, non-delimiters suppressed, is ", "\n");
    field.InsertParagraphNumber = true;
    field.SuppressNonDelimiters = true;

    Assert.AreEqual(" REF  MyBookmark \\n \\t", field.GetFieldCode());

    // Перейти на один уровень списка вниз.
    builder.ListFormat.ListLevelNumber++;
    builder.ListFormat.ListLevel.NumberFormat = ">> \x0001";

    // Отображаем номер списка закладки и номера всех уровней списка над ней.
    field = InsertFieldRef(builder, "MyBookmark", "The bookmark's full context paragraph number is ", "\n");
    field.InsertParagraphNumberInFullContext = true;

    Assert.AreEqual(" REF  MyBookmark \\w", field.GetFieldCode());

    builder.InsertBreak(BreakType.PageBreak);

    // Отображаем номера уровней списка между этим полем REF и закладкой, на которую оно ссылается.
    field = InsertFieldRef(builder, "MyBookmark", "The bookmark's relative paragraph number is ", "\n");
    field.InsertParagraphNumberInRelativeContext = true;

    Assert.AreEqual(" REF  MyBookmark \\r", field.GetFieldCode());

    // В конце документа закладка отобразится здесь как элемент списка.
    builder.Writeln("List level above bookmark");
    builder.ListFormat.ListLevelNumber++;
    builder.ListFormat.ListLevel.NumberFormat = ">>> \x0002";

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.REF.docx");
}

/// <summary>
/// Заставьте конструктор документов вставить поле REF, сослаться на закладку с его помощью и добавить текст до и после него.
/// </summary>
private static FieldRef InsertFieldRef(DocumentBuilder builder, string bookmarkName, string textBefore, string textAfter)
{
    builder.Write(textBefore);
    FieldRef field = (FieldRef)builder.InsertField(FieldType.FieldRef, true);
    field.BookmarkName = bookmarkName;
    builder.Write(textAfter);
    return field;
}
```

### Смотрите также

* class [FieldRef](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
