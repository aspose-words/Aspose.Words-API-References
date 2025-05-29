---
title: FieldIndex Class
linktitle: FieldIndex
articleTitle: FieldIndex
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Fields.FieldIndex, чтобы без усилий реализовать поля INDEX в ваших документах. Улучшите управление документами сегодня!
type: docs
weight: 2470
url: /ru/net/aspose.words.fields/fieldindex/
---
## FieldIndex class

Реализует поле ИНДЕКС.

Чтобы узнать больше, посетите[Работа с полями](https://docs.aspose.com/words/net/working-with-fields/) документальная статья.

```csharp
public class FieldIndex : Field
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [FieldIndex](fieldindex/)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [BookmarkName](../../aspose.words.fields/fieldindex/bookmarkname/) { get; set; } | Возвращает или задает имя закладки, которая отмечает часть документа, используемую для построения индекса. |
| [CrossReferenceSeparator](../../aspose.words.fields/fieldindex/crossreferenceseparator/) { get; set; } | Возвращает или задает последовательность символов, используемую для разделения перекрестных ссылок и других записей. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Получает текст, представляющий отображаемый результат поля. |
| [End](../../aspose.words.fields/field/end/) { get; } | Получает узел, представляющий конец поля. |
| [EntryType](../../aspose.words.fields/fieldindex/entrytype/) { get; set; } | Возвращает или задает тип записи индекса, используемый для построения индекса. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Получает[`FieldFormat`](../fieldformat/)объект, который обеспечивает типизированный доступ к форматированию поля. |
| [HasPageNumberSeparator](../../aspose.words.fields/fieldindex/haspagenumberseparator/) { get; } | Возвращает значение, указывающее, переопределяется ли разделитель номера страницы через код поля. |
| [HasSequenceName](../../aspose.words.fields/fieldindex/hassequencename/) { get; } | Возвращает значение, указывающее, следует ли использовать последовательность при построении результата поля. |
| [Heading](../../aspose.words.fields/fieldindex/heading/) { get; set; } | Возвращает или задает заголовок, который отображается в начале каждого набора записей для любой заданной буквы. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Возвращает или задает, является ли текущий результат поля более неверным (устаревшим) из-за других изменений, внесенных в документ. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Возвращает или задает, заблокировано ли поле (не следует пересчитывать его результат). |
| [LanguageId](../../aspose.words.fields/fieldindex/languageid/) { get; set; } | Возвращает или задает идентификатор языка, используемый для генерации индекса. |
| [LetterRange](../../aspose.words.fields/fieldindex/letterrange/) { get; set; } | Возвращает или задает диапазон букв, которым ограничивается индекс. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Получает или задает LCID поля. |
| [NumberOfColumns](../../aspose.words.fields/fieldindex/numberofcolumns/) { get; set; } | Возвращает или задает количество столбцов на страницу, используемых при построении индекса. |
| [PageNumberListSeparator](../../aspose.words.fields/fieldindex/pagenumberlistseparator/) { get; set; } | Возвращает или задает последовательность символов, которая используется для разделения двух номеров страниц в списке номеров страниц. |
| [PageNumberSeparator](../../aspose.words.fields/fieldindex/pagenumberseparator/) { get; set; } | Возвращает или задает последовательность символов, которая используется для разделения записи индекса и ее номера страницы. |
| [PageRangeSeparator](../../aspose.words.fields/fieldindex/pagerangeseparator/) { get; set; } | Возвращает или задает последовательность символов, которая используется для разделения начала и конца диапазона страниц. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Возвращает или задает текст, который находится между разделителем полей и концом поля. |
| [RunSubentriesOnSameLine](../../aspose.words.fields/fieldindex/runsubentriesonsameline/) { get; set; } | Возвращает или задает, следует ли запускать подзаписи в той же строке, что и основная запись. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Получает узел, представляющий разделитель полей. Может быть`нулевой` . |
| [SequenceName](../../aspose.words.fields/fieldindex/sequencename/) { get; set; } | Возвращает или задает имя последовательности, номер которой включен в номер страницы. |
| [SequenceSeparator](../../aspose.words.fields/fieldindex/sequenceseparator/) { get; set; } | Возвращает или задает последовательность символов, используемую для разделения порядковых номеров и номеров страниц. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Получает узел, представляющий начало поля. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Получает тип поля Microsoft Word. |
| [UseYomi](../../aspose.words.fields/fieldindex/useyomi/) { get; set; } | Возвращает или задает, следует ли включить использование текста yomi для записей индекса. |

## Методы

| Имя | Описание |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Возвращает текст между началом поля и разделителем полей (или концом поля, если разделитель отсутствует). Включаются как код поля, так и результат поля дочерних полей. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Возвращает текст между началом поля и разделителем полей (или концом поля, если разделитель отсутствует). |
| [Remove](../../aspose.words.fields/field/remove/)() | Удаляет поле из документа. Возвращает узел сразу после поля. Если конец поля — последний child его родительского узла, возвращает его родительский абзац. Если поле уже удалено, возвращает`нулевой` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Выполняет отмену связи поля. |
| [Update](../../aspose.words.fields/field/update/)() | Выполняет обновление поля. Выдает исключение, если поле уже обновляется. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Выполняет обновление поля. Выдает исключение, если поле уже обновляется. |

## Примечания

Создает индекс с использованием записей индекса, указанных в полях XE, и вставляет этот индекс в указанное место документа.

## Примеры

Показывает, как создать поле INDEX, а затем использовать поля XE для заполнения его записями.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Создайте поле INDEX, которое будет отображать запись для каждого поля XE, найденного в документе.
// Каждая запись будет отображать значение свойства Text поля XE слева
// и страница, содержащая поле XE справа.
// Если поля XE имеют одинаковое значение в свойстве "Текст",
// поле ИНДЕКС сгруппирует их в одну запись.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// Настройте поле INDEX только для отображения полей XE, которые находятся в пределах границ
// закладки с именем "MainBookmark", свойства "EntryType" которой имеют значение "A".
// Для полей INDEX и XE свойство «EntryType» использует только первый символ своего строкового значения.
index.BookmarkName = "MainBookmark";
index.EntryType = "A";

Assert.AreEqual(" INDEX  \\b MainBookmark \\f A", index.GetFieldCode());

// На новой странице создайте закладку с именем, соответствующим значению
// свойства "BookmarkName" поля INDEX.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark("MainBookmark");

// Поле INDEX выберет эту запись, поскольку она находится внутри закладки,
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

// Завершить закладку и вставить поле XE после нее.
// Он того же типа, что и поле INDEX, но не будет отображаться
// так как он находится за пределами границ закладки.
builder.EndBookmark("MainBookmark");
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 3";
indexEntry.EntryType = "A";

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Filtering.docx");
```

Показывает, как заполнить поле INDEX записями с использованием полей XE, а также изменить его внешний вид.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Создайте поле INDEX, которое будет отображать запись для каждого поля XE, найденного в документе.
// Каждая запись будет отображать значение свойства Text поля XE слева,
// и номер страницы, содержащей поле XE справа.
// Если поля XE имеют одинаковое значение в свойстве "Текст",
// поле ИНДЕКС сгруппирует их в одну запись.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);
index.LanguageId = "1033";

// Установка значения этого свойства на «A» сгруппирует все записи по первой букве,
// и поместите эту букву в верхнем регистре над каждой группой.
index.Heading = "A";

// Задаем таблицу, созданную по полю INDEX, так, чтобы она охватывала 2 столбца.
index.NumberOfColumns = "2";

// Устанавливает, что все записи, начинающиеся с букв, выходящих за пределы диапазона символов «ac», должны быть пропущены.
index.LetterRange = "a-c";

Assert.AreEqual(" INDEX  \\z 1033 \\h A \\c 2 \\p a-c", index.GetFieldCode());

// Следующие два поля XE будут отображаться под заголовком «A»,
// с соответствующими стилями текста, также примененными к номерам страниц.
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

// Следующие два поля XE будут находиться под заголовками «B» и «C» в таблице содержания полей INDEX.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Banana";

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Cherry";

// Поля INDEX сортируют все записи в алфавитном порядке, поэтому эта запись будет отображаться под буквой «A» вместе с двумя другими.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Avocado";

// Эта запись не будет отображаться, так как она начинается с буквы «D»,
// который находится за пределами диапазона символов «ac», определяемого свойством LetterRange поля INDEX.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Durian";

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Formatting.docx");
```

### Смотрите также

* class [Field](../field/)
* пространство имен [Aspose.Words.Fields](../../aspose.words.fields/)
* сборка [Aspose.Words](../../)
