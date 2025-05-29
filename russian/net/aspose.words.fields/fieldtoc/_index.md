---
title: FieldToc Class
linktitle: FieldToc
articleTitle: FieldToc
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Fields.FieldToc для бесшовного создания оглавлений в документах. Улучшите свой рабочий процесс с помощью мощных функций!
type: docs
weight: 2940
url: /ru/net/aspose.words.fields/fieldtoc/
---
## FieldToc class

Реализует поле TOC.

Чтобы узнать больше, посетите[Работа с полями](https://docs.aspose.com/words/net/working-with-fields/) документальная статья.

```csharp
public class FieldToc : Field
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [FieldToc](fieldtoc/)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [BookmarkName](../../aspose.words.fields/fieldtoc/bookmarkname/) { get; set; } | Возвращает или задает имя закладки, которая отмечает часть документа, используемую для построения таблицы. |
| [CaptionlessTableOfFiguresLabel](../../aspose.words.fields/fieldtoc/captionlesstableoffigureslabel/) { get; set; } | Возвращает или задает имя идентификатора последовательности, используемого при построении таблицы рисунков, которая не включает метку и номер подписи . |
| [CustomStyles](../../aspose.words.fields/fieldtoc/customstyles/) { get; set; } | Возвращает или задает список стилей, отличных от встроенных стилей заголовков, для включения в оглавление. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Получает текст, представляющий отображаемый результат поля. |
| [End](../../aspose.words.fields/field/end/) { get; } | Получает узел, представляющий конец поля. |
| [EntryIdentifier](../../aspose.words.fields/fieldtoc/entryidentifier/) { get; set; } | Возвращает или задает строку, которая должна соответствовать идентификаторам типов включаемых полей TC. |
| [EntryLevelRange](../../aspose.words.fields/fieldtoc/entrylevelrange/) { get; set; } | Возвращает или задает диапазон уровней записей таблицы содержания, которые необходимо включить. |
| [EntrySeparator](../../aspose.words.fields/fieldtoc/entryseparator/) { get; set; } | Возвращает или задает последовательность символов, разделяющих запись и ее номер страницы. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Получает[`FieldFormat`](../fieldformat/)объект, который обеспечивает типизированный доступ к форматированию поля. |
| [HeadingLevelRange](../../aspose.words.fields/fieldtoc/headinglevelrange/) { get; set; } | Возвращает или задает диапазон уровней заголовков для включения. |
| [HideInWebLayout](../../aspose.words.fields/fieldtoc/hideinweblayout/) { get; set; } | Возвращает или задает необходимость скрыть заполнитель вкладок и номера страниц в представлении веб-макета. |
| [InsertHyperlinks](../../aspose.words.fields/fieldtoc/inserthyperlinks/) { get; set; } | Возвращает или задает, следует ли делать записи оглавления гиперссылками. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Возвращает или задает, является ли текущий результат поля более неверным (устаревшим) из-за других изменений, внесенных в документ. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Возвращает или задает, заблокировано ли поле (не следует пересчитывать его результат). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Получает или задает LCID поля. |
| [PageNumberOmittingLevelRange](../../aspose.words.fields/fieldtoc/pagenumberomittinglevelrange/) { get; set; } | Возвращает или задает диапазон уровней записей оглавления, из которых следует исключить номера страниц. |
| [PrefixedSequenceIdentifier](../../aspose.words.fields/fieldtoc/prefixedsequenceidentifier/) { get; set; } | Возвращает или задает идентификатор последовательности, для которой следует добавить префикс к номеру страницы записи. |
| [PreserveLineBreaks](../../aspose.words.fields/fieldtoc/preservelinebreaks/) { get; set; } | Возвращает или задает, следует ли сохранять символы новой строки в записях таблицы. |
| [PreserveTabs](../../aspose.words.fields/fieldtoc/preservetabs/) { get; set; } | Возвращает или задает, следует ли сохранять записи табуляции в записях таблицы. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Возвращает или задает текст, который находится между разделителем полей и концом поля. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Получает узел, представляющий разделитель полей. Может быть`нулевой` . |
| [SequenceSeparator](../../aspose.words.fields/fieldtoc/sequenceseparator/) { get; set; } | Возвращает или задает последовательность символов, используемую для разделения порядковых номеров и номеров страниц. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Получает узел, представляющий начало поля. |
| [TableOfFiguresLabel](../../aspose.words.fields/fieldtoc/tableoffigureslabel/) { get; set; } | Возвращает или задает имя идентификатора последовательности, используемого при построении таблицы рисунков. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Получает тип поля Microsoft Word. |
| [UseParagraphOutlineLevel](../../aspose.words.fields/fieldtoc/useparagraphoutlinelevel/) { get; set; } | Возвращает или задает, следует ли использовать примененный уровень структуры абзаца. |

## Методы

| Имя | Описание |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Возвращает текст между началом поля и разделителем полей (или концом поля, если разделитель отсутствует). Включаются как код поля, так и результат поля дочерних полей. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Возвращает текст между началом поля и разделителем полей (или концом поля, если разделитель отсутствует). |
| [Remove](../../aspose.words.fields/field/remove/)() | Удаляет поле из документа. Возвращает узел сразу после поля. Если конец поля — последний child его родительского узла, возвращает его родительский абзац. Если поле уже удалено, возвращает`нулевой` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Выполняет отмену связи поля. |
| [Update](../../aspose.words.fields/field/update/)() | Выполняет обновление поля. Выдает исключение, если поле уже обновляется. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Выполняет обновление поля. Выдает исключение, если поле уже обновляется. |
| [UpdatePageNumbers](../../aspose.words.fields/fieldtoc/updatepagenumbers/)() | Обновляет номера страниц для элементов в этом оглавлении. |

## Примечания

Создает таблицу содержания (которая также может быть таблицей рисунков), используя записи, указанные в полях TC, их уровни заголовков и указанные стили, и вставляет эту таблицу в это место документа.

## Примеры

Показывает, как вставить оглавление и заполнить его записями на основе стилей заголовков.

```csharp
public void FieldToc()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.StartBookmark("MyBookmark");

    // Вставьте поле TOC, которое объединит все заголовки в оглавление.
    // Для каждого заголовка это поле создаст строку с текстом в этом стиле заголовка слева,
    // и страница, на которой заголовок отображается справа.
    FieldToc field = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

    // Используйте свойство BookmarkName только для перечисления заголовков
    // которые появляются в пределах закладки с именем «MyBookmark».
    field.BookmarkName = "MyBookmark";

    // Текст со встроенным стилем заголовка, например «Заголовок 1», примененным к нему, будет считаться заголовком.
    // В этом свойстве мы можем указать дополнительные стили, которые будут использоваться в качестве заголовков оглавлением, а также их уровни оглавления.
    field.CustomStyles = "Quote; 6; Intense Quote; 7";

    // По умолчанию уровни стилей/TOC разделяются в свойстве CustomStyles запятой,
    // но мы можем установить пользовательский разделитель в этом свойстве.
    doc.FieldOptions.CustomTocStyleSeparator = ";";

    // Настройте поле, чтобы исключить все заголовки, уровни TOC которых выходят за пределы этого диапазона.
    field.HeadingLevelRange = "1-3";

    // TOC не будет отображать номера страниц заголовков, уровни TOC которых находятся в этом диапазоне.
    field.PageNumberOmittingLevelRange = "2-5";

     // Задайте пользовательскую строку, которая будет отделять каждый заголовок от номера страницы.
    field.EntrySeparator = "-";
    field.InsertHyperlinks = true;
    field.HideInWebLayout = false;
    field.PreserveLineBreaks = true;
    field.PreserveTabs = true;
    field.UseParagraphOutlineLevel = false;

    InsertNewPageWithHeading(builder, "First entry", "Heading 1");
    builder.Writeln("Paragraph text.");
    InsertNewPageWithHeading(builder, "Second entry", "Heading 1");
    InsertNewPageWithHeading(builder, "Third entry", "Quote");
    InsertNewPageWithHeading(builder, "Fourth entry", "Intense Quote");

    // В этих двух заголовках номера страниц будут опущены, поскольку они находятся в диапазоне «2-5».
    InsertNewPageWithHeading(builder, "Fifth entry", "Heading 2");
    InsertNewPageWithHeading(builder, "Sixth entry", "Heading 3");

    // Эта запись не отображается, поскольку «Заголовок 4» находится за пределами диапазона «1-3», который мы установили ранее.
    InsertNewPageWithHeading(builder, "Seventh entry", "Heading 4");

    builder.EndBookmark("MyBookmark");
    builder.Writeln("Paragraph text.");

    // Эта запись не отображается, поскольку она находится за пределами закладки, указанной в оглавлении.
    InsertNewPageWithHeading(builder, "Eighth entry", "Heading 1");

    Assert.AreEqual(" TOC  \\b MyBookmark \\t \"Quote; 6; Intense Quote; 7\" \\o 1-3 \\n 2-5 \\p - \\h \\x \\w", field.GetFieldCode());

    field.UpdatePageNumbers();
    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.TOC.docx");
}

/// <summary>
/// Начать новую страницу и вставить абзац указанного стиля.
/// </summary>
public void InsertNewPageWithHeading(DocumentBuilder builder, string captionText, string styleName)
{
    builder.InsertBreak(BreakType.PageBreak);
    string originalStyle = builder.ParagraphFormat.StyleName;
    builder.ParagraphFormat.Style = builder.Document.Styles[styleName];
    builder.Writeln(captionText);
    builder.ParagraphFormat.Style = builder.Document.Styles[originalStyle];
}
```

Показывает, как заполнить поле TOC записями с использованием полей SEQ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Поле TOC может создать запись в своей таблице содержания для каждого поля SEQ, найденного в документе.
// Каждая запись содержит абзац, включающий поле SEQ, и номер страницы, на которой находится это поле.
FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

// Поля SEQ отображают счетчик, который увеличивается в каждом поле SEQ.
// Эти поля также поддерживают отдельные подсчеты для каждой уникальной именованной последовательности
// идентифицируется свойством "SequenceIdentifier" поля SEQ.
// Используйте свойство "TableOfFiguresLabel" для наименования основной последовательности для TOC.
// Теперь этот TOC будет создавать записи только из полей SEQ, у которых «SequenceIdentifier» установлен на «MySequence».
fieldToc.TableOfFiguresLabel = "MySequence";

// Мы можем назвать другую последовательность полей SEQ в свойстве "PrefixedSequenceIdentifier".
 // Поля SEQ из этой префиксной последовательности не будут создавать записи TOC.
// Каждая запись TOC, созданная из поля SEQ основной последовательности, теперь также будет отображать количество,
// последовательность префикса в настоящее время находится в поле первичной последовательности SEQ, в котором сделана запись.
fieldToc.PrefixedSequenceIdentifier = "PrefixSequence";

// Каждая запись TOC будет отображать количество префиксов последовательности сразу слева
// номера страницы, на которой отображается поле основной последовательности SEQ.
// Мы можем указать пользовательский разделитель, который будет отображаться между этими двумя числами.
fieldToc.SequenceSeparator = ">";

Assert.AreEqual(" TOC  \\c MySequence \\s PrefixSequence \\d >", fieldToc.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);

// Существует два способа использования полей SEQ для заполнения этого оглавления.
// 1 - Вставка поля SEQ, принадлежащего префиксной последовательности TOC:
// Это поле увеличит количество последовательностей SEQ для "PrefixSequence" на 1.
// Поскольку это поле не принадлежит к основной последовательности, идентифицированной
// свойством "TableOfFiguresLabel" оглавления, оно не будет отображаться как запись.
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "PrefixSequence";
builder.InsertParagraph();

Assert.AreEqual(" SEQ  PrefixSequence", fieldSeq.GetFieldCode());

// 2 - Вставка поля SEQ, принадлежащего основной последовательности TOC:
// Это поле SEQ создаст запись в оглавлении.
// Запись TOC будет содержать абзац, в котором находится поле SEQ, и номер страницы, на которой оно появляется.
// Эта запись также отобразит текущее количество префиксной последовательности,
// отделен от номера страницы значением свойства SeqenceSeparator оглавления.
// Счетчик "PrefixSequence" равен 1, это основное поле последовательности SEQ находится на странице 2,
// и разделитель — «>», поэтому запись будет отображать «1>2».
builder.Write("First TOC entry, MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";

Assert.AreEqual(" SEQ  MySequence", fieldSeq.GetFieldCode());

// Вставьте страницу, увеличьте последовательность префиксов на 2 и вставьте поле SEQ, чтобы впоследствии создать запись TOC.
// Последовательность префикса теперь находится на 2, а поле основной последовательности SEQ находится на странице 3,
// поэтому запись TOC будет отображать «2>3» на своем количестве страниц.
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

* class [Field](../field/)
* пространство имен [Aspose.Words.Fields](../../aspose.words.fields/)
* сборка [Aspose.Words](../../)
