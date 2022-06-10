---
title: FieldCitation
second_title: Справочник по API Aspose.Words для .NET
description: Реализует поле ЦИТАТА.
type: docs
weight: 1510
url: /ru/net/aspose.words.fields/fieldcitation/
---
## FieldCitation class

Реализует поле ЦИТАТА.

```csharp
public class FieldCitation : Field
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [FieldCitation](fieldcitation)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [AnotherSourceTag](../../aspose.words.fields/fieldcitation/anothersourcetag) { get; set; } | Получает или задает значение, соответствующее значению элемента **Tag** другого источника, которое будет включено в цитата. |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | Получает текст, представляющий результат отображаемого поля. |
| [End](../../aspose.words.fields/field/end) { get; } | Получает узел, представляющий конец поля. |
| [Format](../../aspose.words.fields/field/format) { get; } | Получает объект[`FieldFormat`](../fieldformat), предоставляющий типизированный доступ к форматированию поля. |
| [FormatLanguageId](../../aspose.words.fields/fieldcitation/formatlanguageid) { get; set; } | Получает или задает идентификатор языка, который используется в сочетании с указанным библиографическим стилем для форматирования цитаты в документе. |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | Получает или устанавливает, является ли текущий результат поля более неправильным (устаревшим) из-за других изменений, внесенных в документ. |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | Получает или устанавливает, заблокировано ли поле (не должно пересчитывать его результат). |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | Получает или задает LCID поля. |
| [PageNumber](../../aspose.words.fields/fieldcitation/pagenumber) { get; set; } | Получает или задает номер страницы, связанный с цитатой. |
| [Prefix](../../aspose.words.fields/fieldcitation/prefix) { get; set; } | Получает или задает префикс, который добавляется к цитате. |
| [Result](../../aspose.words.fields/field/result) { get; set; } | Получает или задает текст, который находится между разделителем полей и концом поля. |
| [Separator](../../aspose.words.fields/field/separator) { get; } | Получает узел, представляющий разделитель полей. Может быть нулевым. |
| [SourceTag](../../aspose.words.fields/fieldcitation/sourcetag) { get; set; } | Получает или задает значение, соответствующее значению элемента **Tag** источника для вставки. |
| [Start](../../aspose.words.fields/field/start) { get; } | Получает узел, представляющий начало поля. |
| [Suffix](../../aspose.words.fields/fieldcitation/suffix) { get; set; } | Получает или задает суффикс, который добавляется к цитате. |
| [SuppressAuthor](../../aspose.words.fields/fieldcitation/suppressauthor) { get; set; } | Получает или задает, будет ли информация об авторе исключена из цитирования. |
| [SuppressTitle](../../aspose.words.fields/fieldcitation/suppresstitle) { get; set; } | Получает или задает, будет ли информация о заголовке скрыта от цитирования. |
| [SuppressYear](../../aspose.words.fields/fieldcitation/suppressyear) { get; set; } | Получает или задает значение, указывающее, будет ли информация о году скрыта в цитировании. |
| virtual [Type](../../aspose.words.fields/field/type) { get; } | Получает тип поля Microsoft Word. |
| [VolumeNumber](../../aspose.words.fields/fieldcitation/volumenumber) { get; set; } | Получает или задает номер тома, связанный с цитатой. |

## Методы

| Имя | Описание |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)() | Возвращает текст между началом поля и разделителем полей (или концом поля, если разделителя нет). Включены как код поля, так и результат дочерних полей. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)(bool) | Возвращает текст между началом поля и разделителем полей (или концом поля, если разделителя нет). |
| [Remove](../../aspose.words.fields/field/remove)() | Удаляет поле из документа. Возвращает узел сразу после поля. Если конец поля является последним дочерним элементом его родительского узла, возвращает его родительский абзац. Если поле уже удалено, возвращает **null** . |
| [Unlink](../../aspose.words.fields/field/unlink)() | Выполняет развязку поля. |
| [Update](../../aspose.words.fields/field/update)() | Выполняет обновление поля. Выдает, если поле уже обновляется. |
| [Update](../../aspose.words.fields/field/update)(bool) | Выполняет обновление поля. Выдает, если поле уже обновляется. |

### Примечания

Вставляет содержимое **Source**элемент с указанным элементом **Tag** с использованием библиографического стиля.

### Примеры

Показывает, как работать с полями ЦИТАТА и БИБЛИОГРАФИЯ.

```csharp
// Открываем документ, содержащий библиографические источники, которые мы можем найти в
// Microsoft Word через ссылки -> Цитаты и ссылки Библиография -> Управление источниками.
Document doc = new Document(MyDir + "Bibliography.docx");
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Text to be cited with one source.");

// Создать цитату, указав только номер страницы и автора книги, на которую ссылаются.
FieldCitation fieldCitation = (FieldCitation)builder.InsertField(FieldType.FieldCitation, true);

// Мы ссылаемся на источники, используя имена их тегов.
fieldCitation.SourceTag = "Book1";
fieldCitation.PageNumber = "85";
fieldCitation.SuppressAuthor = false;
fieldCitation.SuppressTitle = true;
fieldCitation.SuppressYear = true;

Assert.AreEqual(" CITATION  Book1 \\p 85 \\t \\y", fieldCitation.GetFieldCode());

// Создать более подробную цитату со ссылкой на два источника.
builder.InsertParagraph();
builder.Write("Text to be cited with two sources.");
fieldCitation = (FieldCitation)builder.InsertField(FieldType.FieldCitation, true);
fieldCitation.SourceTag = "Book1";
fieldCitation.AnotherSourceTag = "Book2";
fieldCitation.FormatLanguageId = "en-US";
fieldCitation.PageNumber = "19";
fieldCitation.Prefix = "Prefix ";
fieldCitation.Suffix = " Suffix";
fieldCitation.SuppressAuthor = false;
fieldCitation.SuppressTitle = false;
fieldCitation.SuppressYear = false;
fieldCitation.VolumeNumber = "VII";

Assert.AreEqual(" CITATION  Book1 \\m Book2 \\l en-US \\p 19 \\f \"Prefix \" \\s \" Suffix\" \\v VII", fieldCitation.GetFieldCode());

// Мы можем использовать поле БИБЛИОГРАФИЯ для отображения всех источников в документе.
builder.InsertBreak(BreakType.PageBreak);
FieldBibliography fieldBibliography = (FieldBibliography)builder.InsertField(FieldType.FieldBibliography, true);
fieldBibliography.FormatLanguageId = "1124";

Assert.AreEqual(" BIBLIOGRAPHY  \\l 1124", fieldBibliography.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.CITATION.docx");
```

### Смотрите также

* class [Field](../field)
* пространство имен [Aspose.Words.Fields](../../aspose.words.fields)
* сборка [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
