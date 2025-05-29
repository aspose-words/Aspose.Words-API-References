---
title: FieldOptions Class
linktitle: FieldOptions
articleTitle: FieldOptions
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Fields.FieldOptions, который оптимизирует обработку полей в документах, повышая эффективность рабочего процесса и управления документами.
type: docs
weight: 2660
url: /ru/net/aspose.words.fields/fieldoptions/
---
## FieldOptions class

Представляет параметры управления обработкой полей в документе.

Чтобы узнать больше, посетите[Работа с полями](https://docs.aspose.com/words/net/working-with-fields/) документальная статья.

```csharp
public sealed class FieldOptions
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [BarcodeGenerator](../../aspose.words.fields/fieldoptions/barcodegenerator/) { get; set; } | Получает или задает пользовательский генератор штрихкодов. |
| [BibliographyStylesProvider](../../aspose.words.fields/fieldoptions/bibliographystylesprovider/) { get; set; } | Возвращает или задает поставщика, который возвращает стиль библиографии для [`FieldBibliography`](../fieldbibliography/) и[`FieldCitation`](../fieldcitation/) поля. |
| [BuiltInTemplatesPaths](../../aspose.words.fields/fieldoptions/builtintemplatespaths/) { get; set; } | Получает или задает пути к встроенным шаблонам MS Word. |
| [ComparisonExpressionEvaluator](../../aspose.words.fields/fieldoptions/comparisonexpressionevaluator/) { get; set; } | Возвращает или задает оценщик выражений сравнения полей. |
| [CurrentUser](../../aspose.words.fields/fieldoptions/currentuser/) { get; set; } | Получает или задает информацию о текущем пользователе. |
| [CustomTocStyleSeparator](../../aspose.words.fields/fieldoptions/customtocstyleseparator/) { get; set; } | Получает или задает разделитель пользовательского стиля для переключателя \t в[`FieldToc`](../fieldtoc/) поле. |
| [DefaultDocumentAuthor](../../aspose.words.fields/fieldoptions/defaultdocumentauthor/) { get; set; } | Возвращает или задает имя автора документа по умолчанию. Если имя автора уже указано во встроенных свойствах документа, эта опция не рассматривается. |
| [FieldDatabaseProvider](../../aspose.words.fields/fieldoptions/fielddatabaseprovider/) { get; set; } | Возвращает или задает поставщик, который возвращает результат запроса для[`FieldDatabase`](../fielddatabase/) поле. |
| [FieldIndexFormat](../../aspose.words.fields/fieldoptions/fieldindexformat/) { get; set; } | Получает или задает[`FieldIndexFormat`](./fieldindexformat/) что представляет форматирование для[`FieldIndex`](../fieldindex/) поля в документе. |
| [FieldUpdateCultureProvider](../../aspose.words.fields/fieldoptions/fieldupdatecultureprovider/) { get; set; } | Возвращает или задает поставщик, который возвращает объект культуры, специфичный для каждого конкретного поля. |
| [FieldUpdateCultureSource](../../aspose.words.fields/fieldoptions/fieldupdateculturesource/) { get; set; } | Указывает, какую культуру использовать для форматирования результата поля. |
| [FieldUpdatingCallback](../../aspose.words.fields/fieldoptions/fieldupdatingcallback/) { get; set; } | Получает или устанавливает[`IFieldUpdatingCallback`](../ifieldupdatingcallback/) реализация |
| [FieldUpdatingProgressCallback](../../aspose.words.fields/fieldoptions/fieldupdatingprogresscallback/) { get; set; } | Получает или устанавливает[`IFieldUpdatingProgressCallback`](../ifieldupdatingprogresscallback/) реализация. |
| [FileName](../../aspose.words.fields/fieldoptions/filename/) { get; set; } | Возвращает или задает имя файла документа. |
| [IsBidiTextSupportedOnUpdate](../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/) { get; set; } | Возвращает или задает значение, указывающее, полностью ли поддерживается двунаправленный текст во время обновления поля. |
| [LegacyNumberFormat](../../aspose.words.fields/fieldoptions/legacynumberformat/) { get; set; } | Возвращает или задает значение, указывающее, включен ли устаревший (более ранний, чем AW 13.10) числовой формат для полей. |
| [PreProcessCulture](../../aspose.words.fields/fieldoptions/preprocessculture/) { get; set; } | Возвращает или задает культуру для предварительной обработки значений полей. |
| [ResultFormatter](../../aspose.words.fields/fieldoptions/resultformatter/) { get; set; } | Позволяет контролировать форматирование результата поля. |
| [TemplateName](../../aspose.words.fields/fieldoptions/templatename/) { get; set; } | Возвращает или задает имя файла шаблона, используемого документом. |
| [ToaCategories](../../aspose.words.fields/fieldoptions/toacategories/) { get; set; } | Получает или задает таблицу категорий полномочий. |
| [UseInvariantCultureNumberFormat](../../aspose.words.fields/fieldoptions/useinvariantculturenumberformat/) { get; set; } | Возвращает или задает значение, указывающее, анализируется ли числовой формат с использованием инвариантной культуры или нет |
| [UserPromptRespondent](../../aspose.words.fields/fieldoptions/userpromptrespondent/) { get; set; } | Получает или задает респонденту подсказки пользователя во время обновления поля. |

## Примеры

Показывает, как указать источник культуры, используемый для форматирования даты во время обновления полей или слияния почты.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте два поля слияния с немецкой локалью.
builder.Font.LocaleId = new CultureInfo("de-DE").LCID;
builder.InsertField("MERGEFIELD Date1 \\@ \"dddd, d MMMM yyyy\"");
builder.Write(" - ");
builder.InsertField("MERGEFIELD Date2 \\@ \"dddd, d MMMM yyyy\"");

// Установите текущий язык и региональные параметры на американский английский, сохранив исходное значение в переменной.
CultureInfo currentCulture = Thread.CurrentThread.CurrentCulture;
Thread.CurrentThread.CurrentCulture = new CultureInfo("en-US");

// Это слияние будет использовать региональные параметры текущего потока для форматирования даты — американский английский.
doc.MailMerge.Execute(new[] { "Date1" }, new object[] { new DateTime(2020, 1, 01) });

// Настройте следующее слияние для получения значения культуры из кода поля. Значение этой культуры будет немецким.
doc.FieldOptions.FieldUpdateCultureSource = FieldUpdateCultureSource.FieldCode;
doc.MailMerge.Execute(new[] { "Date2" }, new object[] { new DateTime(2020, 1, 01) });

// Первый результат слияния содержит дату, отформатированную на английском языке, а второй — на немецком.
Assert.AreEqual("Wednesday, 1 January 2020 - Mittwoch, 1 Januar 2020", doc.Range.Text.Trim());

// Восстановить исходную культуру потока.
Thread.CurrentThread.CurrentCulture = currentCulture;
```

### Смотрите также

* пространство имен [Aspose.Words.Fields](../../aspose.words.fields/)
* сборка [Aspose.Words](../../)
