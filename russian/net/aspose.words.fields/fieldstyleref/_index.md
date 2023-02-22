---
title: Class FieldStyleRef
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Fields.FieldStyleRef сорт. Реализует поле STYLEREF.
type: docs
weight: 2290
url: /ru/net/aspose.words.fields/fieldstyleref/
---
## FieldStyleRef class

Реализует поле STYLEREF.

```csharp
public class FieldStyleRef : Field
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [FieldStyleRef](fieldstyleref/)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Получает текст, представляющий результат отображаемого поля. |
| [End](../../aspose.words.fields/field/end/) { get; } | Получает узел, представляющий конец поля. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Получает[`FieldFormat`](../fieldformat/) объект, предоставляющий типизированный доступ к форматированию поля. |
| [InsertParagraphNumber](../../aspose.words.fields/fieldstyleref/insertparagraphnumber/) { get; set; } | Получает или задает, следует ли вставлять номер абзаца, на который указывает ссылка, точно так, как он отображается в документе. |
| [InsertParagraphNumberInFullContext](../../aspose.words.fields/fieldstyleref/insertparagraphnumberinfullcontext/) { get; set; } | Получает или задает, следует ли вставлять номер абзаца, на который указывает ссылка, в полном контексте. |
| [InsertParagraphNumberInRelativeContext](../../aspose.words.fields/fieldstyleref/insertparagraphnumberinrelativecontext/) { get; set; } | Получает или задает, следует ли вставлять номер абзаца, на который указывает ссылка, в относительном контексте. |
| [InsertRelativePosition](../../aspose.words.fields/fieldstyleref/insertrelativeposition/) { get; set; } | Получает или задает, следует ли вставлять относительное положение абзаца, на который делается ссылка. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Получает или устанавливает, является ли текущий результат поля более неверным (устаревшим) из-за других изменений, внесенных в документ. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Получает или задает, заблокировано ли поле (не следует пересчитывать его результат). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Получает или задает LCID поля. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Получает или задает текст, который находится между разделителем поля и концом поля. |
| [SearchFromBottom](../../aspose.words.fields/fieldstyleref/searchfrombottom/) { get; set; } | Получает или задает, следует ли искать снизу текущей страницы, а не сверху. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Получает узел, представляющий разделитель полей. Может быть нулевым. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Получает узел, представляющий начало поля. |
| [StyleName](../../aspose.words.fields/fieldstyleref/stylename/) { get; set; } | Получает или задает имя стиля, по которому форматируется искомый текст. |
| [SuppressNonDelimiters](../../aspose.words.fields/fieldstyleref/suppressnondelimiters/) { get; set; } | Получает или задает, следует ли подавлять символы, не являющиеся разделителями. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Получает тип поля Microsoft Word. |

## Методы

| Имя | Описание |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделителя нет). Включены как код поля, так и результат поля дочерних полей. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | Возвращает текст между началом поля и разделителем полей (или концом поля, если разделителя нет). |
| [Remove](../../aspose.words.fields/field/remove/)() | Удаляет поле из документа. Возвращает узел сразу после поля. Если конец поля является последним child его родительского узла, возвращает его родительский абзац. Если поле уже удалено, возвращает **нулевой** . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Выполняет развязку поля. |
| [Update](../../aspose.words.fields/field/update/)() | Выполняет обновление поля. Выдает, если поле уже обновляется. |
| [Update](../../aspose.words.fields/field/update/)(bool) | Выполняет обновление поля. Выдает, если поле уже обновляется. |

### Примечания

STYLEREF используется для ссылки на фрагмент текста в документе, отформатированном с использованием указанного стиля.

### Примеры

Показывает, как использовать поля STYLEREF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Создать список на основе шаблона списка Microsoft Word.
Aspose.Words.Lists.List list = doc.Lists.Add(Aspose.Words.Lists.ListTemplate.NumberDefault);

// Этот сгенерированный список будет отображать "1.a)".
 // Пробел перед скобкой — это символ, не являющийся разделителем, который мы можем подавить.
list.ListLevels[0].NumberFormat = "\x0000.";
list.ListLevels[1].NumberFormat = "\x0001 )";

// Добавляем текст и применяем стили абзаца, на которые будут ссылаться поля STYLEREF.
builder.ListFormat.List = list;
builder.ListFormat.ListIndent();
builder.ParagraphFormat.Style = doc.Styles["List Paragraph"];
builder.Writeln("Item 1");
builder.ParagraphFormat.Style = doc.Styles["Quote"];
builder.Writeln("Item 2");
builder.ParagraphFormat.Style = doc.Styles["List Paragraph"];
builder.Writeln("Item 3");
builder.ListFormat.RemoveNumbers();
builder.ParagraphFormat.Style = doc.Styles["Normal"];

// Поместите поле STYLEREF в заголовок и отобразите первый текст в стиле «List Paragraph» в документе.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
FieldStyleRef field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "List Paragraph";

// Поместите поле STYLEREF в нижний колонтитул, чтобы оно отображало последний текст.
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "List Paragraph";
field.SearchFromBottom = true;

builder.MoveToDocumentEnd();

// Мы также можем использовать поля STYLEREF для ссылки на номера списков.
builder.Write("\nParagraph number: ");
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "Quote";
field.InsertParagraphNumber = true;

builder.Write("\nParagraph number, relative context: ");
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "Quote";
field.InsertParagraphNumberInRelativeContext = true;

builder.Write("\nParagraph number, full context: ");
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "Quote";
field.InsertParagraphNumberInFullContext = true;

builder.Write("\nParagraph number, full context, non-delimiter chars suppressed: ");
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "Quote";
field.InsertParagraphNumberInFullContext = true;
field.SuppressNonDelimiters = true;

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.STYLEREF.docx");
```

### Смотрите также

* class [Field](../field/)
* пространство имен [Aspose.Words.Fields](../../aspose.words.fields/)
* сборка [Aspose.Words](../../)


