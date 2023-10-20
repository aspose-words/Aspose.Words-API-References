---
title: FieldRef.IncludeNoteOrComment
linktitle: IncludeNoteOrComment
articleTitle: IncludeNoteOrComment
second_title: Aspose.Words для .NET
description: FieldRef IncludeNoteOrComment свойство. Получает или задает следует ли увеличивать номера сносок концевых сносок и примечаний которые отмечены закладкой и вставлять соответствующие сноски концевые сноски и текст комментария на С#.
type: docs
weight: 30
url: /ru/net/aspose.words.fields/fieldref/includenoteorcomment/
---
## FieldRef.IncludeNoteOrComment property

Получает или задает, следует ли увеличивать номера сносок, концевых сносок и примечаний, которые отмечены закладкой, и вставлять соответствующие сноски, концевые сноски и текст комментария.

```csharp
public bool IncludeNoteOrComment { get; set; }
```

## Примеры

Показывает, как вставлять поля REF в ссылочные закладки.

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

    // Мы применим собственный формат списка, в котором количество угловых скобок указывает уровень списка, на котором мы сейчас находимся.
    builder.ListFormat.ApplyNumberDefault();
    builder.ListFormat.ListLevel.NumberFormat = "> \x0000";

    // Вставляем поле REF, которое будет содержать текст внутри нашей закладки, действовать как гиперссылка и клонировать сноски закладки.
    FieldRef field = InsertFieldRef(builder, "MyBookmark", "", "\n");
    field.IncludeNoteOrComment = true;
    field.InsertHyperlink = true;

    Assert.AreEqual(" REF  MyBookmark \\f \\h", field.GetFieldCode());

    // Вставляем поле REF и отображаем, находится ли указанная закладка выше или ниже него.
    field = InsertFieldRef(builder, "MyBookmark", "The referenced paragraph is ", " this field.\n");
    field.InsertRelativePosition = true;

    Assert.AreEqual(" REF  MyBookmark \\p", field.GetFieldCode());

    // Отображение номера закладки в списке, как он отображается в документе.
    field = InsertFieldRef(builder, "MyBookmark", "The bookmark's paragraph number is ", "\n");
    field.InsertParagraphNumber = true;

    Assert.AreEqual(" REF  MyBookmark \\n", field.GetFieldCode());

    // Отобразить номер списка закладок, но без опущенных символов, не являющихся разделителями, таких как угловые скобки.
    field = InsertFieldRef(builder, "MyBookmark", "The bookmark's paragraph number, non-delimiters suppressed, is ", "\n");
    field.InsertParagraphNumber = true;
    field.SuppressNonDelimiters = true;

    Assert.AreEqual(" REF  MyBookmark \\n \\t", field.GetFieldCode());

    // Переход на один уровень списка вниз.
    builder.ListFormat.ListLevelNumber++;
    builder.ListFormat.ListLevel.NumberFormat = ">> \x0001";

    // Отображение номера закладки в списке и номеров всех уровней списка над ней.
    field = InsertFieldRef(builder, "MyBookmark", "The bookmark's full context paragraph number is ", "\n");
    field.InsertParagraphNumberInFullContext = true;

    Assert.AreEqual(" REF  MyBookmark \\w", field.GetFieldCode());

    builder.InsertBreak(BreakType.PageBreak);

    // Отобразить номера уровней списка между этим полем REF и закладкой, на которую оно ссылается.
    field = InsertFieldRef(builder, "MyBookmark", "The bookmark's relative paragraph number is ", "\n");
    field.InsertParagraphNumberInRelativeContext = true;

    Assert.AreEqual(" REF  MyBookmark \\r", field.GetFieldCode());

    // В конце документа закладка появится здесь как элемент списка.
    builder.Writeln("List level above bookmark");
    builder.ListFormat.ListLevelNumber++;
    builder.ListFormat.ListLevel.NumberFormat = ">>> \x0002";

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.REF.docx");
}

/// <summary>
/// Заставьте конструктор документов вставить поле REF, ссылаться на закладку и добавить текст до и после него.
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
