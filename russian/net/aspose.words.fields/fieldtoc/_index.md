---
title: FieldToc
second_title: Справочник по API Aspose.Words для .NET
description: Реализует поле TOC.
type: docs
weight: 2340
url: /ru/net/aspose.words.fields/fieldtoc/
---
## FieldToc class

Реализует поле TOC.

```csharp
public class FieldToc : Field
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [FieldToc](fieldtoc)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [BookmarkName](../../aspose.words.fields/fieldtoc/bookmarkname) { get; set; } | Получает или задает имя закладки, которая отмечает часть документа, используемую для построения таблицы. |
| [CaptionlessTableOfFiguresLabel](../../aspose.words.fields/fieldtoc/captionlesstableoffigureslabel) { get; set; } | Получает или задает имя идентификатора последовательности, используемого при построении таблицы рисунков, которая не включает метку и номер заголовка . |
| [CustomStyles](../../aspose.words.fields/fieldtoc/customstyles) { get; set; } | Получает или задает список стилей, отличных от встроенных стилей заголовков, для включения в оглавление. |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | Получает текст, представляющий результат отображаемого поля. |
| [End](../../aspose.words.fields/field/end) { get; } | Получает узел, представляющий конец поля. |
| [EntryIdentifier](../../aspose.words.fields/fieldtoc/entryidentifier) { get; set; } | Получает или задает строку, которая должна соответствовать идентификаторам типов включаемых полей TC. |
| [EntryLevelRange](../../aspose.words.fields/fieldtoc/entrylevelrange) { get; set; } | Получает или задает диапазон уровней включаемых записей оглавления. |
| [EntrySeparator](../../aspose.words.fields/fieldtoc/entryseparator) { get; set; } | Получает или задает последовательность символов, разделяющую запись и номер ее страницы. |
| [Format](../../aspose.words.fields/field/format) { get; } | Получает объект[`FieldFormat`](../fieldformat), предоставляющий типизированный доступ к форматированию поля. |
| [HeadingLevelRange](../../aspose.words.fields/fieldtoc/headinglevelrange) { get; set; } | Получает или задает диапазон уровней заголовков для включения. |
| [HideInWebLayout](../../aspose.words.fields/fieldtoc/hideinweblayout) { get; set; } | Получает или задает, следует ли скрывать закладку и номера страниц в представлении веб-макета. |
| [InsertHyperlinks](../../aspose.words.fields/fieldtoc/inserthyperlinks) { get; set; } | Получает или задает, следует ли делать записи оглавления гиперссылками. |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | Получает или устанавливает, является ли текущий результат поля более неправильным (устаревшим) из-за других изменений, внесенных в документ. |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | Получает или устанавливает, заблокировано ли поле (не должно пересчитывать его результат). |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | Получает или задает LCID поля. |
| [PageNumberOmittingLevelRange](../../aspose.words.fields/fieldtoc/pagenumberomittinglevelrange) { get; set; } | Получает или задает диапазон уровней записей оглавления, из которых исключаются номера страниц. |
| [PrefixedSequenceIdentifier](../../aspose.words.fields/fieldtoc/prefixedsequenceidentifier) { get; set; } | Получает или задает идентификатор последовательности, для которой к номеру страницы записи следует добавить префикс. |
| [PreserveLineBreaks](../../aspose.words.fields/fieldtoc/preservelinebreaks) { get; set; } | Получает или задает, следует ли сохранять символы новой строки в записях таблицы. |
| [PreserveTabs](../../aspose.words.fields/fieldtoc/preservetabs) { get; set; } | Получает или задает, следует ли сохранять записи вкладок в записях таблицы. |
| [Result](../../aspose.words.fields/field/result) { get; set; } | Получает или задает текст, который находится между разделителем полей и концом поля. |
| [Separator](../../aspose.words.fields/field/separator) { get; } | Получает узел, представляющий разделитель полей. Может быть нулевым. |
| [SequenceSeparator](../../aspose.words.fields/fieldtoc/sequenceseparator) { get; set; } | Получает или задает последовательность символов, используемую для разделения порядковых номеров и номеров страниц. |
| [Start](../../aspose.words.fields/field/start) { get; } | Получает узел, представляющий начало поля. |
| [TableOfFiguresLabel](../../aspose.words.fields/fieldtoc/tableoffigureslabel) { get; set; } | Получает или задает имя идентификатора последовательности, используемого при построении таблицы рисунков. |
| virtual [Type](../../aspose.words.fields/field/type) { get; } | Получает тип поля Microsoft Word. |
| [UseParagraphOutlineLevel](../../aspose.words.fields/fieldtoc/useparagraphoutlinelevel) { get; set; } | Получает или задает, следует ли использовать примененный уровень структуры абзаца. |

## Методы

| Имя | Описание |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)() | Возвращает текст между началом поля и разделителем полей (или концом поля, если разделителя нет). Включены как код поля, так и результат дочерних полей. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)(bool) | Возвращает текст между началом поля и разделителем полей (или концом поля, если разделителя нет). |
| [Remove](../../aspose.words.fields/field/remove)() | Удаляет поле из документа. Возвращает узел сразу после поля. Если конец поля является последним дочерним элементом его родительского узла, возвращает его родительский абзац. Если поле уже удалено, возвращает **null** . |
| [Unlink](../../aspose.words.fields/field/unlink)() | Выполняет развязку поля. |
| [Update](../../aspose.words.fields/field/update)() | Выполняет обновление поля. Выдает, если поле уже обновляется. |
| [Update](../../aspose.words.fields/field/update)(bool) | Выполняет обновление поля. Выдает, если поле уже обновляется. |
| [UpdatePageNumbers](../../aspose.words.fields/fieldtoc/updatepagenumbers)() | Обновляет номера страниц для элементов в этом оглавлении. |

### Примечания

Создает оглавление (которое также может быть таблицей рисунков), используя записи, указанные параметром Поля TC, их уровни заголовков и указанные стили, и вставляет эту таблицу в это место в документе.

### Примеры

Показывает, как вставить оглавление и заполнить его записями на основе стилей заголовков.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Поле TOC может создать запись в своем содержании для каждого поля SEQ, найденного в документе.
// Каждая запись содержит абзац, содержащий поле SEQ, и номер страницы, на которой появляется это поле.
FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

// В полях SEQ отображается счетчик, который увеличивается в каждом поле SEQ.
// Эти поля также поддерживают отдельные счетчики для каждой уникальной именованной последовательности
// определяется свойством "SequenceIdentifier" поля SEQ.
// Используйте свойство «TableOfFiguresLabel», чтобы назвать основную последовательность для TOC.
// Теперь этот оглавление будет создавать только записи из полей SEQ с их «SequenceIdentifier», установленным на «MySequence».
fieldToc.TableOfFiguresLabel = "MySequence";

// Мы можем назвать другую последовательность полей SEQ в свойстве "PrefixedSequenceIdentifier".
 // Поля SEQ из этой последовательности префиксов не будут создавать записи TOC.
// Каждая запись TOC, созданная из поля SEQ основной последовательности, теперь также будет отображать количество, которое
// последовательность префикса в настоящее время включена в поле SEQ первичной последовательности, которое сделало запись.
fieldToc.PrefixedSequenceIdentifier = "PrefixSequence";

// Каждая запись TOC будет отображать счетчик последовательностей префиксов сразу слева
// номера страницы, на которой появляется поле SEQ основной последовательности.
// Мы можем указать собственный разделитель, который будет отображаться между этими двумя числами.
fieldToc.SequenceSeparator = ">";

Assert.AreEqual(" TOC  \\c MySequence \\s PrefixSequence \\d >", fieldToc.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);

// Существует два способа использования полей SEQ для заполнения этого оглавления.
// 1 - Вставка поля SEQ, принадлежащего префиксной последовательности TOC:
// Это поле увеличит счетчик последовательности SEQ для «PrefixSequence» на 1.
// Так как это поле не принадлежит идентифицированной основной последовательности
// по свойству "TableOfFiguresLabel" оглавления оно не будет отображаться как запись.
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "PrefixSequence";
builder.InsertParagraph();

Assert.AreEqual(" SEQ  PrefixSequence", fieldSeq.GetFieldCode());

// 2 - Вставка поля SEQ, принадлежащего основной последовательности TOC:
// Это поле SEQ создаст запись в оглавлении.
// Запись TOC будет содержать абзац, в котором находится поле SEQ, и номер страницы, на которой оно появляется.
// Эта запись также будет отображать счетчик, на котором в данный момент находится последовательность префиксов,
// отделяется от номера страницы значением свойства SeqenceSeparator оглавления.
// Счетчик «PrefixSequence» равен 1, это поле SEQ основной последовательности находится на странице 2,
// и разделитель ">", поэтому запись будет отображать "1>2".
builder.Write("First TOC entry, MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";

Assert.AreEqual(" SEQ  MySequence", fieldSeq.GetFieldCode());

// Вставьте страницу, продвиньте последовательность префиксов на 2 и вставьте поле SEQ, чтобы впоследствии создать запись оглавления.
// Последовательность префикса теперь равна 2, а поле SEQ основной последовательности находится на странице 3,
// таким образом, запись оглавления будет отображать "2>3" на количестве страниц.
builder.InsertBreak(BreakType.PageBreak);
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "PrefixSequence";
builder.InsertParagraph();
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
builder.Write("Second TOC entry, MySequence #");
fieldSeq.SequenceIdentifier = "MySequence";

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.TOC.SEQ.docx");
```

Показывает, как заполнить поле TOC записями, используя поля SEQ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Поле TOC может создать запись в своем содержании для каждого поля SEQ, найденного в документе.
// Каждая запись содержит абзац, содержащий поле SEQ, и номер страницы, на которой появляется это поле.
FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

// В полях SEQ отображается счетчик, который увеличивается в каждом поле SEQ.
// Эти поля также поддерживают отдельные счетчики для каждой уникальной именованной последовательности
// определяется свойством "SequenceIdentifier" поля SEQ.
// Используйте свойство «TableOfFiguresLabel», чтобы назвать основную последовательность для TOC.
// Теперь этот оглавление будет создавать только записи из полей SEQ с их «SequenceIdentifier», установленным на «MySequence».
fieldToc.TableOfFiguresLabel = "MySequence";

// Мы можем назвать другую последовательность полей SEQ в свойстве "PrefixedSequenceIdentifier".
 // Поля SEQ из этой последовательности префиксов не будут создавать записи TOC.
// Каждая запись TOC, созданная из поля SEQ основной последовательности, теперь также будет отображать количество, которое
// последовательность префикса в настоящее время включена в поле SEQ первичной последовательности, которое сделало запись.
fieldToc.PrefixedSequenceIdentifier = "PrefixSequence";

// Каждая запись TOC будет отображать счетчик последовательностей префиксов сразу слева
// номера страницы, на которой появляется поле SEQ основной последовательности.
// Мы можем указать собственный разделитель, который будет отображаться между этими двумя числами.
fieldToc.SequenceSeparator = ">";

Assert.AreEqual(" TOC  \\c MySequence \\s PrefixSequence \\d >", fieldToc.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);

// Существует два способа использования полей SEQ для заполнения этого оглавления.
// 1 - Вставка поля SEQ, принадлежащего префиксной последовательности TOC:
// Это поле увеличит счетчик последовательности SEQ для «PrefixSequence» на 1.
// Так как это поле не принадлежит идентифицированной основной последовательности
// по свойству "TableOfFiguresLabel" оглавления оно не будет отображаться как запись.
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "PrefixSequence";
builder.InsertParagraph();

Assert.AreEqual(" SEQ  PrefixSequence", fieldSeq.GetFieldCode());

// 2 - Вставка поля SEQ, принадлежащего основной последовательности TOC:
// Это поле SEQ создаст запись в оглавлении.
// Запись TOC будет содержать абзац, в котором находится поле SEQ, и номер страницы, на которой оно появляется.
// Эта запись также будет отображать счетчик, на котором в данный момент находится последовательность префиксов,
// отделяется от номера страницы значением свойства SeqenceSeparator оглавления.
// Счетчик «PrefixSequence» равен 1, это поле SEQ основной последовательности находится на странице 2,
// и разделитель ">", поэтому запись будет отображать "1>2".
builder.Write("First TOC entry, MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";

Assert.AreEqual(" SEQ  MySequence", fieldSeq.GetFieldCode());

// Вставьте страницу, продвиньте последовательность префиксов на 2 и вставьте поле SEQ, чтобы впоследствии создать запись оглавления.
// Последовательность префикса теперь равна 2, а поле SEQ основной последовательности находится на странице 3,
// таким образом, запись оглавления будет отображать "2>3" на количестве страниц.
builder.InsertBreak(BreakType.PageBreak);
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "PrefixSequence";
builder.InsertParagraph();
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
builder.Write("Second TOC entry, MySequence #");
fieldSeq.SequenceIdentifier = "MySequence";

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.TOC.SEQ.docx");
```

### Смотрите также

* class [Field](../field)
* пространство имен [Aspose.Words.Fields](../../aspose.words.fields)
* сборка [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
