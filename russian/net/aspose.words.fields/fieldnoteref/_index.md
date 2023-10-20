---
title: FieldNoteRef Class
linktitle: FieldNoteRef
articleTitle: FieldNoteRef
second_title: Aspose.Words для .NET
description: Aspose.Words.Fields.FieldNoteRef сорт. Реализует поле ПРИМЕЧАНИЕ на С#.
type: docs
weight: 2200
url: /ru/net/aspose.words.fields/fieldnoteref/
---
## FieldNoteRef class

Реализует поле ПРИМЕЧАНИЕ.

Чтобы узнать больше, посетите[Работа с полями](https://docs.aspose.com/words/net/working-with-fields/) статья документации.

```csharp
public class FieldNoteRef : Field
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [FieldNoteRef](fieldnoteref/)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [BookmarkName](../../aspose.words.fields/fieldnoteref/bookmarkname/) { get; set; } | Получает или задает имя закладки. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Получает текст, представляющий результат отображаемого поля. |
| [End](../../aspose.words.fields/field/end/) { get; } | Получает узел, представляющий конец поля. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Получает[`FieldFormat`](../fieldformat/) объект, обеспечивающий типизированный доступ к форматированию поля. |
| [InsertHyperlink](../../aspose.words.fields/fieldnoteref/inserthyperlink/) { get; set; } | Получает или задает необходимость вставки гиперссылки на абзац, отмеченный закладкой. |
| [InsertReferenceMark](../../aspose.words.fields/fieldnoteref/insertreferencemark/) { get; set; } | Вставляет ссылочный знак с тем же форматированием символов, что и стиль ссылки на сноску или ссылку на концевую сноску. |
| [InsertRelativePosition](../../aspose.words.fields/fieldnoteref/insertrelativeposition/) { get; set; } | Получает или задает, следует ли вставлять относительную позицию абзаца, отмеченного закладкой. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Получает или устанавливает, является ли текущий результат поля более неправильным (устаревшим) из-за других изменений, внесенных в документ. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Получает или задает, заблокировано ли поле (не следует пересчитывать результат). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Получает или задает LCID поля. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Получает или задает текст, расположенный между разделителем полей и концом поля. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Получает узел, представляющий разделитель полей. Возможно`нулевой` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Получает узел, представляющий начало поля. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Получает тип поля Microsoft Word. |

## Методы

| Имя | Описание |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделителя нет). Включены как код поля, так и результат поля дочерних полей. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Возвращает текст между началом поля и разделителем полей (или концом поля, если разделителя нет). |
| [Remove](../../aspose.words.fields/field/remove/)() | Удаляет поле из документа. Возвращает узел сразу после поля. Если конец поля является последним дочерним его родительского узла, возвращает его родительский абзац. Если поле уже удалено, возвращается`нулевой` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Выполняет отсоединение поля. |
| [Update](../../aspose.words.fields/field/update/)() | Выполняет обновление поля. Выдает, если поле уже обновляется. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Выполняет обновление поля. Выдает, если поле уже обновляется. |

## Примечания

Вставляет метку сноски или концевой сноски, отмеченную указанной закладкой.

## Примеры

Показывает, как создать перекрестную ссылку на сноски с помощью поля ПРИМЕЧАНИЕ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("CrossReference: ");

FieldNoteRef field = (FieldNoteRef)builder.InsertField(FieldType.FieldNoteRef, false); // <--- не обновлять поле
field.BookmarkName = "CrossRefBookmark";
field.InsertHyperlink = true;
field.InsertReferenceMark = true;
field.InsertRelativePosition = false;
builder.Writeln();

builder.StartBookmark("CrossRefBookmark");
builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Footnote, "Cross referenced footnote.");
builder.EndBookmark("CrossRefBookmark");
builder.Writeln();            

doc.UpdateFields();           

// Это поле работает только в старых версиях Microsoft Word.
doc.Save(ArtifactsDir + "Field.NOTEREF.doc");
```

Показывает, как вставить поля NOTEREF и изменить их внешний вид.

```csharp
public void FieldNoteRef()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Создайте закладку со сноской, на которую будет ссылаться поле ПРИМЕЧАНИЕ.
    InsertBookmarkWithFootnote(builder, "MyBookmark1", "Contents of MyBookmark1", "Footnote from MyBookmark1");

    // В этом поле ПРИМЕЧАНИЕРЕФ будет отображаться номер сноски внутри указанной закладки.
    // Установка свойства InsertHyperlink позволяет нам перейти к закладке, удерживая Ctrl + щелкнув поле в Microsoft Word.
    Assert.AreEqual(" NOTEREF  MyBookmark2 \\h",
        InsertFieldNoteRef(builder, "MyBookmark2", true, false, false, "Hyperlink to Bookmark2, with footnote number ").GetFieldCode());

    // При использовании флага \p после номера сноски поле также отображает положение закладки относительно поля.
    // Bookmark1 находится над этим полем и содержит сноску номер 1, поэтому при обновлении результатом будет «1 выше».
    Assert.AreEqual(" NOTEREF  MyBookmark1 \\h \\p",
        InsertFieldNoteRef(builder, "MyBookmark1", true, true, false, "Bookmark1, with footnote number ").GetFieldCode());

    // Bookmark2 находится под этим полем и содержит сноску номер 2, поэтому в поле будет отображаться «2 ниже».
    // Флаг \f заставляет число 2 отображаться в том же формате, что и метка номера сноски в реальном тексте.
    Assert.AreEqual(" NOTEREF  MyBookmark2 \\h \\p \\f",
        InsertFieldNoteRef(builder, "MyBookmark2", true, true, true, "Bookmark2, with footnote number ").GetFieldCode());

    builder.InsertBreak(BreakType.PageBreak);
    InsertBookmarkWithFootnote(builder, "MyBookmark2", "Contents of MyBookmark2", "Footnote from MyBookmark2");

    doc.UpdatePageLayout();
    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.NOTEREF.docx");
}

/// <summary>
/// Использует построитель документов для вставки поля NOTEREF с указанными свойствами.
/// </summary>
private static FieldNoteRef InsertFieldNoteRef(DocumentBuilder builder, string bookmarkName, bool insertHyperlink, bool insertRelativePosition, bool insertReferenceMark, string textBefore)
{
    builder.Write(textBefore);

    FieldNoteRef field = (FieldNoteRef)builder.InsertField(FieldType.FieldNoteRef, true);
    field.BookmarkName = bookmarkName;
    field.InsertHyperlink = insertHyperlink;
    field.InsertRelativePosition = insertRelativePosition;
    field.InsertReferenceMark = insertReferenceMark;
    builder.Writeln();

    return field;
}

/// <summary>
/// Использует конструктор документов для вставки именованной закладки со сноской в конце.
/// </summary>
private static void InsertBookmarkWithFootnote(DocumentBuilder builder, string bookmarkName, string bookmarkText, string footnoteText)
{
    builder.StartBookmark(bookmarkName);
    builder.Write(bookmarkText);
    builder.InsertFootnote(FootnoteType.Footnote, footnoteText);
    builder.EndBookmark(bookmarkName);
    builder.Writeln();
}
```

### Смотрите также

* class [Field](../field/)
* пространство имен [Aspose.Words.Fields](../../aspose.words.fields/)
* сборка [Aspose.Words](../../)
