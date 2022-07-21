---
title: FieldRef
second_title: Справочник по API Aspose.Words для .NET
description: Реализует поле REF.
type: docs
weight: 2180
url: /ru/net/aspose.words.fields/fieldref/
---
## FieldRef class

Реализует поле REF.

```csharp
public class FieldRef : Field
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [FieldRef](fieldref)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [BookmarkName](../../aspose.words.fields/fieldref/bookmarkname) { get; set; } | Получает или задает имя закладки, на которую указывает ссылка. |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | Получает текст, представляющий результат отображаемого поля. |
| [End](../../aspose.words.fields/field/end) { get; } | Получает узел, представляющий конец поля. |
| [Format](../../aspose.words.fields/field/format) { get; } | Получает[`FieldFormat`](../fieldformat) объект, предоставляющий типизированный доступ к форматированию поля. |
| [IncludeNoteOrComment](../../aspose.words.fields/fieldref/includenoteorcomment) { get; set; } | Получает или задает, нужно ли увеличивать номера сносок, концевых сносок и аннотаций, которые помечены закладкой, и вставлять соответствующие сноски, концевые сноски и текст комментариев. |
| [InsertHyperlink](../../aspose.words.fields/fieldref/inserthyperlink) { get; set; } | Получает или задает, следует ли создавать гиперссылку на отмеченный закладкой абзац. |
| [InsertParagraphNumber](../../aspose.words.fields/fieldref/insertparagraphnumber) { get; set; } | Получает или задает, следует ли вставлять номер абзаца, на который указывает ссылка, точно так, как он отображается в документе. |
| [InsertParagraphNumberInFullContext](../../aspose.words.fields/fieldref/insertparagraphnumberinfullcontext) { get; set; } | Получает или задает, следует ли вставлять номер абзаца, на который указывает ссылка, в полном контексте. |
| [InsertParagraphNumberInRelativeContext](../../aspose.words.fields/fieldref/insertparagraphnumberinrelativecontext) { get; set; } | Получает или задает, следует ли вставлять номер абзаца, на который указывает ссылка, в относительном контексте. |
| [InsertRelativePosition](../../aspose.words.fields/fieldref/insertrelativeposition) { get; set; } | Получает или задает, следует ли вставлять относительное положение абзаца, на который делается ссылка. |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | Получает или устанавливает, является ли текущий результат поля более неверным (устаревшим) из-за других изменений, внесенных в документ. |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | Получает или задает, заблокировано ли поле (не следует пересчитывать его результат). |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | Получает или задает LCID поля. |
| [NumberSeparator](../../aspose.words.fields/fieldref/numberseparator) { get; set; } | Получает или задает последовательность символов, используемую для разделения порядковых номеров и номеров страниц. |
| [Result](../../aspose.words.fields/field/result) { get; set; } | Получает или задает текст, который находится между разделителем поля и концом поля. |
| [Separator](../../aspose.words.fields/field/separator) { get; } | Получает узел, представляющий разделитель полей. Может быть нулевым. |
| [Start](../../aspose.words.fields/field/start) { get; } | Получает узел, представляющий начало поля. |
| [SuppressNonDelimiters](../../aspose.words.fields/fieldref/suppressnondelimiters) { get; set; } | Получает или задает, следует ли подавлять символы, не являющиеся разделителями. |
| virtual [Type](../../aspose.words.fields/field/type) { get; } | Получает тип поля Microsoft Word. |

## Методы

| Имя | Описание |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)() | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделителя нет). Включены как код поля, так и результат поля дочерних полей. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)(bool) | Возвращает текст между началом поля и разделителем полей (или концом поля, если разделителя нет). |
| [Remove](../../aspose.words.fields/field/remove)() | Удаляет поле из документа. Возвращает узел сразу после поля. Если конец поля является последним child его родительского узла, возвращает его родительский абзац. Если поле уже удалено, возвращает **нулевой** . |
| [Unlink](../../aspose.words.fields/field/unlink)() | Выполняет развязку поля. |
| [Update](../../aspose.words.fields/field/update)() | Выполняет обновление поля. Выдает, если поле уже обновляется. |
| [Update](../../aspose.words.fields/field/update)(bool) | Выполняет обновление поля. Выдает, если поле уже обновляется. |

### Примечания

Вставляет текст или графику, представленные указанной закладкой.

### Примеры

Показывает, как создать закладку для текста с помощью поля SET, а затем отобразить его в документе с помощью поля REF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

 // Назовите текст с закладкой с помощью поля SET.
// Это поле относится к «закладке», а не к структуре закладок, которая появляется в тексте, а к именованной переменной.
FieldSet fieldSet = (FieldSet)builder.InsertField(FieldType.FieldSet, false);
fieldSet.BookmarkName = "MyBookmark";
fieldSet.BookmarkText = "Hello world!";
fieldSet.Update();

Assert.AreEqual(" SET  MyBookmark \"Hello world!\"", fieldSet.GetFieldCode());

// Обращаемся к закладке по имени в поле REF и отображаем ее содержимое.
FieldRef fieldRef = (FieldRef)builder.InsertField(FieldType.FieldRef, true);
fieldRef.BookmarkName = "MyBookmark";
fieldRef.Update();

Assert.AreEqual(" REF  MyBookmark", fieldRef.GetFieldCode());
Assert.AreEqual("Hello world!", fieldRef.Result);

doc.Save(ArtifactsDir + "Field.SET.REF.docx");
```

Показывает, как вставлять поля REF в ссылки на закладки.

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

    // Мы применим пользовательский формат списка, где количество угловых скобок указывает уровень списка, на котором мы находимся в данный момент.
    builder.ListFormat.ApplyNumberDefault();
    builder.ListFormat.ListLevel.NumberFormat = "> \x0000";

    // Вставьте поле REF, которое будет содержать текст в нашей закладке, действовать как гиперссылка и клонировать сноски закладки.
    FieldRef field = InsertFieldRef(builder, "MyBookmark", "", "\n");
    field.IncludeNoteOrComment = true;
    field.InsertHyperlink = true;

    Assert.AreEqual(" REF  MyBookmark \\f \\h", field.GetFieldCode());

    // Вставьте поле REF и отобразите, находится ли указанная закладка выше или ниже него.
    field = InsertFieldRef(builder, "MyBookmark", "The referenced paragraph is ", " this field.\n");
    field.InsertRelativePosition = true;

    Assert.AreEqual(" REF  MyBookmark \\p", field.GetFieldCode());

    // Показать номер закладки в списке, как он отображается в документе.
    field = InsertFieldRef(builder, "MyBookmark", "The bookmark's paragraph number is ", "\n");
    field.InsertParagraphNumber = true;

    Assert.AreEqual(" REF  MyBookmark \\n", field.GetFieldCode());

    // Показать номер списка закладок, но без символов-разделителей, таких как угловые скобки.
    field = InsertFieldRef(builder, "MyBookmark", "The bookmark's paragraph number, non-delimiters suppressed, is ", "\n");
    field.InsertParagraphNumber = true;
    field.SuppressNonDelimiters = true;

    Assert.AreEqual(" REF  MyBookmark \\n \\t", field.GetFieldCode());

    // Переход вниз на один уровень списка.
    builder.ListFormat.ListLevelNumber++;
    builder.ListFormat.ListLevel.NumberFormat = ">> \x0001";

    // Отображаем номер списка закладки и номера всех уровней списка над ней.
    field = InsertFieldRef(builder, "MyBookmark", "The bookmark's full context paragraph number is ", "\n");
    field.InsertParagraphNumberInFullContext = true;

    Assert.AreEqual(" REF  MyBookmark \\w", field.GetFieldCode());

    builder.InsertBreak(BreakType.PageBreak);

    // Показать номера уровня списка между этим полем REF и закладкой, на которую оно ссылается.
    field = InsertFieldRef(builder, "MyBookmark", "The bookmark's relative paragraph number is ", "\n");
    field.InsertParagraphNumberInRelativeContext = true;

    Assert.AreEqual(" REF  MyBookmark \\r", field.GetFieldCode());

    // В конце документа закладка будет отображаться здесь как элемент списка.
    builder.Writeln("List level above bookmark");
    builder.ListFormat.ListLevelNumber++;
    builder.ListFormat.ListLevel.NumberFormat = ">>> \x0002";

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.REF.docx");

/// <summary>
/// Заставьте конструктор документа вставить поле REF, сослаться на закладку с ним и добавить текст до и после него.
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

* class [Field](../field)
* пространство имен [Aspose.Words.Fields](../../aspose.words.fields)
* сборка [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
