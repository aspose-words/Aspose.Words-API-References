---
title: FieldOptions
second_title: Справочник по API Aspose.Words для .NET
description: Представляет параметры для управления обработкой полей в документе.
type: docs
weight: 2060
url: /ru/net/aspose.words.fields/fieldoptions/
---
## FieldOptions class

Представляет параметры для управления обработкой полей в документе.

```csharp
public sealed class FieldOptions
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [BarcodeGenerator](../../aspose.words.fields/fieldoptions/barcodegenerator) { get; set; } | Получает или устанавливает собственный генератор штрих-кода. |
| [BuiltInTemplatesPaths](../../aspose.words.fields/fieldoptions/builtintemplatespaths) { get; set; } | Получает или задает пути к встроенным шаблонам MS Word. |
| [ComparisonExpressionEvaluator](../../aspose.words.fields/fieldoptions/comparisonexpressionevaluator) { get; set; } | Получает или задает средство оценки выражений сравнения полей. |
| [CurrentUser](../../aspose.words.fields/fieldoptions/currentuser) { get; set; } | Получает или задает информацию о текущем пользователе. |
| [CustomTocStyleSeparator](../../aspose.words.fields/fieldoptions/customtocstyleseparator) { get; set; } | Получает или устанавливает разделитель пользовательского стиля для переключателя \t в поле[`FieldToc`](../fieldtoc). |
| [DefaultDocumentAuthor](../../aspose.words.fields/fieldoptions/defaultdocumentauthor) { get; set; } | Получает или устанавливает имя автора документа по умолчанию. Если имя автора уже указано во встроенных свойствах документа, этот параметр не учитывается. |
| [FieldIndexFormat](../../aspose.words.fields/fieldoptions/fieldindexformat) { get; set; } | Получает или задает[`FieldIndexFormat`](./fieldindexformat)который представляет форматирование для поля[`FieldIndex`](../fieldindex)в документе. |
| [FieldUpdateCultureProvider](../../aspose.words.fields/fieldoptions/fieldupdatecultureprovider) { get; set; } | Получает или задает поставщика, который возвращает объект культуры для каждого конкретного поля. |
| [FieldUpdateCultureSource](../../aspose.words.fields/fieldoptions/fieldupdateculturesource) { get; set; } | Указывает, какую культуру использовать для форматирования результата поля. |
| [FieldUpdatingCallback](../../aspose.words.fields/fieldoptions/fieldupdatingcallback) { get; set; } | Получает или устанавливает[`IFieldUpdatingCallback`](../ifieldupdatingcallback)реализация |
| [FileName](../../aspose.words.fields/fieldoptions/filename) { get; set; } | Получает или задает имя файла документа. |
| [IsBidiTextSupportedOnUpdate](../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate) { get; set; } | Получает или задает значение, указывающее, полностью ли поддерживается двунаправленный текст во время обновления поля. |
| [LegacyNumberFormat](../../aspose.words.fields/fieldoptions/legacynumberformat) { get; set; } | Получает или задает значение, указывающее, включен ли устаревший (до AW 13.10) числовой формат для полей или нет. |
| [PreProcessCulture](../../aspose.words.fields/fieldoptions/preprocessculture) { get; set; } | Получает или задает культуру для предварительной обработки значений полей. |
| [ResultFormatter](../../aspose.words.fields/fieldoptions/resultformatter) { get; set; } | Позволяет управлять форматированием результата поля. |
| [TemplateName](../../aspose.words.fields/fieldoptions/templatename) { get; set; } | Получает или задает имя файла шаблона, используемого документом. |
| [ToaCategories](../../aspose.words.fields/fieldoptions/toacategories) { get; set; } | Получает или задает таблицу категорий полномочий. |
| [UseInvariantCultureNumberFormat](../../aspose.words.fields/fieldoptions/useinvariantculturenumberformat) { get; set; } | Получает или задает значение, указывающее, анализируется ли числовой формат с использованием инвариантного языка и региональных параметров |
| [UserPromptRespondent](../../aspose.words.fields/fieldoptions/userpromptrespondent) { get; set; } | Получает или задает респондента на запросы пользователя во время обновления поля. |

### Примеры

Показывает, как указать источник языка и региональных параметров, используемых для форматирования даты во время обновления поля или слияния.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

 // Вставляем два поля слияния с немецкой локалью.
builder.Font.LocaleId = new CultureInfo("de-DE").LCID;
builder.InsertField("MERGEFIELD Date1 \\@ \"dddd, d MMMM yyyy\"");
builder.Write(" - ");
builder.InsertField("MERGEFIELD Date2 \\@ \"dddd, d MMMM yyyy\"");

 // Установите текущую культуру на американский английский после сохранения исходного значения в переменной.
CultureInfo currentCulture = Thread.CurrentThread.CurrentCulture;
Thread.CurrentThread.CurrentCulture = new CultureInfo("en-US");

 // Это слияние будет использовать культуру текущего потока для форматирования даты, английский язык США.
doc.MailMerge.Execute(new[] { "Date1" }, new object[] { new DateTime(2020, 1, 01) });

// Настройте следующее слияние, чтобы получить значение культуры из кода поля. Значение этой культуры будет немецким.
doc.FieldOptions.FieldUpdateCultureSource = FieldUpdateCultureSource.FieldCode;
doc.MailMerge.Execute(new[] { "Date2" }, new object[] { new DateTime(2020, 1, 01) });

 // Первый результат слияния содержит дату в английском формате, а второй — в немецком.
Assert.AreEqual("Wednesday, 1 January 2020 - Mittwoch, 1 Januar 2020", doc.Range.Text.Trim());

 // Восстановить исходную культуру потока.
Thread.CurrentThread.CurrentCulture = currentCulture;
```

### Смотрите также

* пространство имен [Aspose.Words.Fields](../../aspose.words.fields)
* сборка [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
