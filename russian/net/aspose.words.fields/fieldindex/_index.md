---
title: FieldIndex
second_title: Справочник по API Aspose.Words для .NET
description: Реализует поле ИНДЕКС.
type: docs
weight: 1910
url: /ru/net/aspose.words.fields/fieldindex/
---
## FieldIndex class

Реализует поле ИНДЕКС.

```csharp
public class FieldIndex : Field
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [FieldIndex](fieldindex)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [BookmarkName](../../aspose.words.fields/fieldindex/bookmarkname) { get; set; } | Получает или задает имя закладки, которая отмечает часть документа, используемую для построения индекса. |
| [CrossReferenceSeparator](../../aspose.words.fields/fieldindex/crossreferenceseparator) { get; set; } | Получает или задает последовательность символов, используемую для разделения перекрестных ссылок и других записей. |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | Получает текст, представляющий результат отображаемого поля. |
| [End](../../aspose.words.fields/field/end) { get; } | Получает узел, представляющий конец поля. |
| [EntryType](../../aspose.words.fields/fieldindex/entrytype) { get; set; } | Получает или задает тип записи индекса, используемый для построения индекса. |
| [Format](../../aspose.words.fields/field/format) { get; } | Получает[`FieldFormat`](../fieldformat) объект, предоставляющий типизированный доступ к форматированию поля. |
| [HasPageNumberSeparator](../../aspose.words.fields/fieldindex/haspagenumberseparator) { get; } | Получает значение, указывающее, переопределяется ли разделитель номеров страниц кодом поля. |
| [HasSequenceName](../../aspose.words.fields/fieldindex/hassequencename) { get; } | Получает значение, указывающее, следует ли использовать последовательность при построении результатов поля. |
| [Heading](../../aspose.words.fields/fieldindex/heading) { get; set; } | Получает или задает заголовок, который появляется в начале каждого набора записей для любой заданной буквы. |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | Получает или устанавливает, является ли текущий результат поля более неверным (устаревшим) из-за других изменений, внесенных в документ. |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | Получает или задает, заблокировано ли поле (не следует пересчитывать его результат). |
| [LanguageId](../../aspose.words.fields/fieldindex/languageid) { get; set; } | Получает или задает идентификатор языка, используемый для создания индекса. |
| [LetterRange](../../aspose.words.fields/fieldindex/letterrange) { get; set; } | Получает или задает диапазон букв, которым ограничивается индекс. |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | Получает или задает LCID поля. |
| [NumberOfColumns](../../aspose.words.fields/fieldindex/numberofcolumns) { get; set; } | Получает или задает количество столбцов на странице, используемых при построении индекса. |
| [PageNumberListSeparator](../../aspose.words.fields/fieldindex/pagenumberlistseparator) { get; set; } | Получает или задает последовательность символов, используемую для разделения двух номеров страниц в списке номеров страниц. |
| [PageNumberSeparator](../../aspose.words.fields/fieldindex/pagenumberseparator) { get; set; } | Получает или задает последовательность символов, используемую для разделения записи указателя и ее номера страницы. |
| [PageRangeSeparator](../../aspose.words.fields/fieldindex/pagerangeseparator) { get; set; } | Получает или задает последовательность символов, используемую для разделения начала и конца диапазона страниц. |
| [Result](../../aspose.words.fields/field/result) { get; set; } | Получает или задает текст, который находится между разделителем поля и концом поля. |
| [RunSubentriesOnSameLine](../../aspose.words.fields/fieldindex/runsubentriesonsameline) { get; set; } | Получает или задает, следует ли запускать подзаписи в той же строке, что и основная запись. |
| [Separator](../../aspose.words.fields/field/separator) { get; } | Получает узел, представляющий разделитель полей. Может быть нулевым. |
| [SequenceName](../../aspose.words.fields/fieldindex/sequencename) { get; set; } | Получает или задает имя последовательности, номер которой включен в номер страницы. |
| [SequenceSeparator](../../aspose.words.fields/fieldindex/sequenceseparator) { get; set; } | Получает или задает последовательность символов, используемую для разделения порядковых номеров и номеров страниц. |
| [Start](../../aspose.words.fields/field/start) { get; } | Получает узел, представляющий начало поля. |
| virtual [Type](../../aspose.words.fields/field/type) { get; } | Получает тип поля Microsoft Word. |
| [UseYomi](../../aspose.words.fields/fieldindex/useyomi) { get; set; } | Получает или задает, следует ли включить использование текста yomi для элементов указателя. |

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

Создает индекс, используя записи индекса, указанные в полях XE, и вставляет этот индекс в это место в документе.

### Примеры

Показывает, как создать поле INDEX, а затем использовать поля XE для заполнения его записями.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Создать поле INDEX, которое будет отображать запись для каждого поля XE, найденного в документе.
// Каждая запись будет отображать значение свойства Text поля XE с левой стороны
// и страница, содержащая поле XE справа.
// Если поля XE имеют одинаковое значение в свойстве «Текст»,
// поле ИНДЕКС сгруппирует их в одну запись.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// Настройте поле INDEX только для отображения полей XE, которые находятся в пределах границ
// закладки с именем "MainBookmark", чьи свойства "EntryType" имеют значение "A".
// Для полей INDEX и XE свойство EntryType использует только первый символ своего строкового значения.
index.BookmarkName = "MainBookmark";
index.EntryType = "A";

Assert.AreEqual(" INDEX  \\b MainBookmark \\f A", index.GetFieldCode());

// На новой странице запускаем закладку с именем, совпадающим со значением
// свойства "ИмяЗакладки" поля ИНДЕКС.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark("MainBookmark");

// Поле ИНДЕКС выберет эту запись, потому что она находится внутри закладки,
// и его тип записи также соответствует типу записи поля INDEX.
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 1";
indexEntry.EntryType = "A";

Assert.AreEqual(" XE  \"Index entry 1\" \\f A", indexEntry.GetFieldCode());

// Вставьте поле XE, которое не будет отображаться в ИНДЕКСЕ, поскольку типы записей не совпадают.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 2";
indexEntry.EntryType = "B";

// Завершить закладку и затем вставить поле XE.
// Оно того же типа, что и поле ИНДЕКС, но не будет отображаться
// так как он находится за пределами закладки.
builder.EndBookmark("MainBookmark");
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 3";
indexEntry.EntryType = "A";

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Filtering.docx");
```

Показывает, как заполнить поле INDEX записями, используя поля XE, а также изменить его внешний вид.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Создать поле INDEX, которое будет отображать запись для каждого поля XE, найденного в документе.
// Каждая запись будет отображать значение свойства Text поля XE с левой стороны,
// и номер страницы, содержащей поле XE справа.
// Если поля XE имеют одинаковое значение в свойстве «Текст»,
// поле ИНДЕКС сгруппирует их в одну запись.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);
index.LanguageId = "1033";

// Установка значения этого свойства в "A" сгруппирует все записи по их первой букве,
// и поместите эту букву в верхнем регистре над каждой группой.
index.Heading = "A";

// Устанавливаем таблицу, созданную полем INDEX, на 2 столбца.
index.NumberOfColumns = "2";

// Установить, что любые записи с начальными буквами за пределами диапазона символов "ac" должны быть опущены.
index.LetterRange = "a-c";

Assert.AreEqual(" INDEX  \\z 1033 \\h A \\c 2 \\p a-c", index.GetFieldCode());

// Следующие два поля XE будут отображаться под заголовком «A»,
// с их соответствующими стилями текста, которые также применяются к их номерам страниц.
builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Apple";
indexEntry.IsItalic = true;

Assert.AreEqual(" XE  Apple \\i", indexEntry.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Apricot";
indexEntry.IsBold = true;

Assert.AreEqual(" XE  Apricot \\b", indexEntry.GetFieldCode());

// Оба следующих двух поля XE будут под заголовками "B" и "C" в таблице содержания полей INDEX.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Banana";

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Cherry";

// Поля ИНДЕКС сортируют все записи в алфавитном порядке, поэтому эта запись будет отображаться под буквой «А» вместе с двумя другими.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Avocado";

// Эта запись не появится, потому что она начинается с буквы "D",
// который находится за пределами диапазона символов "ac", определяемого свойством LetterRange поля INDEX.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Durian";

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Formatting.docx");
```

### Смотрите также

* class [Field](../field)
* пространство имен [Aspose.Words.Fields](../../aspose.words.fields)
* сборка [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
