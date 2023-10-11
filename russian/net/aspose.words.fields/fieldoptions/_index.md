---
title: Class FieldOptions
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Fields.FieldOptions сорт. Представляет параметры управления обработкой полей в документе.
type: docs
weight: 2250
url: /ru/net/aspose.words.fields/fieldoptions/
---
## FieldOptions class

Представляет параметры управления обработкой полей в документе.

Чтобы узнать больше, посетите[Работа с полями](https://docs.aspose.com/words/net/working-with-fields/) статья документации.

```csharp
public sealed class FieldOptions
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [BarcodeGenerator](../../aspose.words.fields/fieldoptions/barcodegenerator/) { get; set; } | Получает или устанавливает собственный генератор штрих-кода. |
| [BibliographyStylesProvider](../../aspose.words.fields/fieldoptions/bibliographystylesprovider/) { get; set; } | Получает или задает поставщика, который возвращает стиль библиографии для [`FieldBibliography`](../fieldbibliography/) и[`FieldCitation`](../fieldcitation/) поля. |
| [BuiltInTemplatesPaths](../../aspose.words.fields/fieldoptions/builtintemplatespaths/) { get; set; } | Получает или задает пути к встроенным шаблонам MS Word. |
| [ComparisonExpressionEvaluator](../../aspose.words.fields/fieldoptions/comparisonexpressionevaluator/) { get; set; } | Получает или задает оценщик выражений сравнения полей. |
| [CurrentUser](../../aspose.words.fields/fieldoptions/currentuser/) { get; set; } | Получает или задает информацию о текущем пользователе. |
| [CustomTocStyleSeparator](../../aspose.words.fields/fieldoptions/customtocstyleseparator/) { get; set; } | Получает или задает собственный разделитель стилей для переключателя \t в[`FieldToc`](../fieldtoc/) поле. |
| [DefaultDocumentAuthor](../../aspose.words.fields/fieldoptions/defaultdocumentauthor/) { get; set; } | Получает или задает имя автора документа по умолчанию. Если имя автора уже указано во встроенных свойствах документа, этот параметр не учитывается. |
| [FieldDatabaseProvider](../../aspose.words.fields/fieldoptions/fielddatabaseprovider/) { get; set; } | Получает или задает поставщика, который возвращает результат запроса для[`FieldDatabase`](../fielddatabase/) поле. |
| [FieldIndexFormat](../../aspose.words.fields/fieldoptions/fieldindexformat/) { get; set; } | Получает или устанавливает[`FieldIndexFormat`](./fieldindexformat/) который представляет форматирование для[`FieldIndex`](../fieldindex/) поля в документе. |
| [FieldUpdateCultureProvider](../../aspose.words.fields/fieldoptions/fieldupdatecultureprovider/) { get; set; } | Получает или задает поставщика, который возвращает объект культуры, специфичный для каждого конкретного поля. |
| [FieldUpdateCultureSource](../../aspose.words.fields/fieldoptions/fieldupdateculturesource/) { get; set; } | Указывает, какой язык и региональные параметры использовать для форматирования результата поля. |
| [FieldUpdatingCallback](../../aspose.words.fields/fieldoptions/fieldupdatingcallback/) { get; set; } | Получает или устанавливает[`IFieldUpdatingCallback`](../ifieldupdatingcallback/) реализация |
| [FieldUpdatingProgressCallback](../../aspose.words.fields/fieldoptions/fieldupdatingprogresscallback/) { get; set; } | Получает или устанавливает[`IFieldUpdatingProgressCallback`](../ifieldupdatingprogresscallback/) реализация. |
| [FileName](../../aspose.words.fields/fieldoptions/filename/) { get; set; } | Получает или задает имя файла документа. |
| [IsBidiTextSupportedOnUpdate](../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/) { get; set; } | Получает или задает значение, указывающее, полностью ли поддерживается двунаправленный текст во время обновления поля или нет. |
| [LegacyNumberFormat](../../aspose.words.fields/fieldoptions/legacynumberformat/) { get; set; } | Получает или задает значение, указывающее, включен или нет устаревший (ранний, чем AW 13.10) числовой формат для полей. |
| [PreProcessCulture](../../aspose.words.fields/fieldoptions/preprocessculture/) { get; set; } | Получает или задает язык и региональные параметры для предварительной обработки значений полей. |
| [ResultFormatter](../../aspose.words.fields/fieldoptions/resultformatter/) { get; set; } | Позволяет контролировать форматирование результата поля. |
| [TemplateName](../../aspose.words.fields/fieldoptions/templatename/) { get; set; } | Получает или задает имя файла шаблона, используемого документом. |
| [ToaCategories](../../aspose.words.fields/fieldoptions/toacategories/) { get; set; } | Получает или задает таблицу категорий полномочий. |
| [UseInvariantCultureNumberFormat](../../aspose.words.fields/fieldoptions/useinvariantculturenumberformat/) { get; set; } | Получает или задает значение, указывающее, что числовой формат анализируется с использованием инвариантного языка и региональных параметров или нет |
| [UserPromptRespondent](../../aspose.words.fields/fieldoptions/userpromptrespondent/) { get; set; } | Получает или задает респондента на запросы пользователя во время обновления поля. |

### Примеры

Показывает, как указать источник языка и региональных параметров, используемый для форматирования даты во время обновления поля или слияния почты.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставляем два поля слияния с немецкой локалью.
builder.Font.LocaleId = new CultureInfo("de-DE").LCID;
builder.InsertField("MERGEFIELD Date1 \\@ \"dddd, d MMMM yyyy\"");
builder.Write(" - ");
builder.InsertField("MERGEFIELD Date2 \\@ \"dddd, d MMMM yyyy\"");

// Установите текущую культуру на английский (США) после сохранения исходного значения в переменной.
CultureInfo currentCulture = Thread.CurrentThread.CurrentCulture;
Thread.CurrentThread.CurrentCulture = new CultureInfo("en-US");

// Это слияние будет использовать культуру текущего потока для форматирования даты (американский английский).
doc.MailMerge.Execute(new[] { "Date1" }, new object[] { new DateTime(2020, 1, 01) });

// Настройте следующее слияние для получения значения культуры из кода поля. Ценность этой культуры будет немецкой.
doc.FieldOptions.FieldUpdateCultureSource = FieldUpdateCultureSource.FieldCode;
doc.MailMerge.Execute(new[] { "Date2" }, new object[] { new DateTime(2020, 1, 01) });

// Первый результат слияния содержит дату, отформатированную на английском языке, а второй — на немецком.
Assert.AreEqual("Wednesday, 1 January 2020 - Mittwoch, 1 Januar 2020", doc.Range.Text.Trim());

// Восстанавливаем исходную культуру потока.
Thread.CurrentThread.CurrentCulture = currentCulture;
```

### Смотрите также

* пространство имен [Aspose.Words.Fields](../../aspose.words.fields/)
* сборка [Aspose.Words](../../)


