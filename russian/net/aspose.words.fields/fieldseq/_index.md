---
title: FieldSeq
second_title: Справочник по API Aspose.Words для .NET
description: Реализует поле SEQ.
type: docs
weight: 2240
url: /ru/net/aspose.words.fields/fieldseq/
---
## FieldSeq class

Реализует поле SEQ.

```csharp
public class FieldSeq : Field
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [FieldSeq](fieldseq)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [BookmarkName](../../aspose.words.fields/fieldseq/bookmarkname) { get; set; } | Получает или задает имя закладки, которое ссылается на элемент в другом месте документа, а не в текущем местоположении. |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | Получает текст, представляющий результат отображаемого поля. |
| [End](../../aspose.words.fields/field/end) { get; } | Получает узел, представляющий конец поля. |
| [Format](../../aspose.words.fields/field/format) { get; } | Получает[`FieldFormat`](../fieldformat) объект, предоставляющий типизированный доступ к форматированию поля. |
| [InsertNextNumber](../../aspose.words.fields/fieldseq/insertnextnumber) { get; set; } | Получает или задает, следует ли вставлять следующий порядковый номер для указанного элемента. |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | Получает или устанавливает, является ли текущий результат поля более неверным (устаревшим) из-за других изменений, внесенных в документ. |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | Получает или задает, заблокировано ли поле (не следует пересчитывать его результат). |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | Получает или задает LCID поля. |
| [ResetHeadingLevel](../../aspose.words.fields/fieldseq/resetheadinglevel) { get; set; } | Получает или задает целое число, представляющее уровень заголовка, на который сбрасывается порядковый номер. Возвращает -1, если номер отсутствует. |
| [ResetNumber](../../aspose.words.fields/fieldseq/resetnumber) { get; set; } | Получает или задает целое число для сброса порядкового номера. Возвращает -1, если число отсутствует. |
| [Result](../../aspose.words.fields/field/result) { get; set; } | Получает или задает текст, который находится между разделителем поля и концом поля. |
| [Separator](../../aspose.words.fields/field/separator) { get; } | Получает узел, представляющий разделитель полей. Может быть нулевым. |
| [SequenceIdentifier](../../aspose.words.fields/fieldseq/sequenceidentifier) { get; set; } | Получает или задает имя, назначенное серии элементов, которые должны быть пронумерованы. |
| [Start](../../aspose.words.fields/field/start) { get; } | Получает узел, представляющий начало поля. |
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

Последовательная нумерация глав, таблиц, рисунков и других определяемых пользователем списков элементов в документе.

### Примеры

Показывает создание нумерации с использованием полей SEQ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// В полях SEQ отображается счетчик, который увеличивается в каждом поле SEQ.
// Эти поля также поддерживают отдельные счетчики для каждой уникальной именованной последовательности
// определяется свойством "SequenceIdentifier" поля SEQ.
// Вставьте поле SEQ, которое будет отображать текущее значение счетчика «MySequence»,
// после использования свойства "ResetNumber", чтобы установить его в 100.
builder.Write("#");
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.ResetNumber = "100";
fieldSeq.Update();

Assert.AreEqual(" SEQ  MySequence \\r 100", fieldSeq.GetFieldCode());
Assert.AreEqual("100", fieldSeq.Result);

// Показать следующее число в этой последовательности с другим полем SEQ.
builder.Write(", #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.Update();

Assert.AreEqual("101", fieldSeq.Result);

// Вставить заголовок уровня 1.
builder.InsertBreak(BreakType.ParagraphBreak);
builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("This level 1 heading will reset MySequence to 1");
builder.ParagraphFormat.Style = doc.Styles["Normal"];

// Вставьте другое поле SEQ из той же последовательности и настройте его для сброса счетчика в каждом заголовке с 1.
builder.Write("\n#");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.ResetHeadingLevel = "1";
fieldSeq.Update();

// Приведенный выше заголовок является заголовком уровня 1, поэтому счетчик для этой последовательности сбрасывается на 1.
Assert.AreEqual(" SEQ  MySequence \\s 1", fieldSeq.GetFieldCode());
Assert.AreEqual("1", fieldSeq.Result);

// Переход к следующему номеру этой последовательности.
builder.Write(", #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.InsertNextNumber = true;
fieldSeq.Update();

Assert.AreEqual(" SEQ  MySequence \\n", fieldSeq.GetFieldCode());
Assert.AreEqual("2", fieldSeq.Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.SEQ.ResetNumbering.docx");
```

Показывает, как объединить оглавление и поля последовательности.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Поле TOC может создать запись в своем содержании для каждого поля SEQ, найденного в документе.
// Каждая запись содержит абзац, содержащий поле SEQ,
// и номер страницы, на которой отображается поле.
FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

// Настройте это поле TOC, чтобы оно имело свойство SequenceIdentifier со значением "MySequence".
fieldToc.TableOfFiguresLabel = "MySequence";

// Настройте это поле TOC, чтобы выбирать только те поля SEQ, которые находятся в пределах закладки
// с именем "TOCBookmark".
fieldToc.BookmarkName = "TOCBookmark";
builder.InsertBreak(BreakType.PageBreak);

Assert.AreEqual(" TOC  \\c MySequence \\b TOCBookmark", fieldToc.GetFieldCode());

// В полях SEQ отображается счетчик, который увеличивается в каждом поле SEQ.
// Эти поля также поддерживают отдельные счетчики для каждой уникальной именованной последовательности
// определяется свойством "SequenceIdentifier" поля SEQ.
// Вставляем поле SEQ с идентификатором последовательности, совпадающим с оглавлением
// Свойство TableOfFiguresLabel. Это поле не создаст запись в оглавлении, так как оно находится за пределами
// границы закладки, обозначенные "BookmarkName".
builder.Write("MySequence #");
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
builder.Writeln(", will not show up in the TOC because it is outside of the bookmark.");

builder.StartBookmark("TOCBookmark");

// Последовательность этого поля SEQ соответствует свойству TableOfFiguresLabel оглавления и находится в пределах границ закладки.
// Абзац, содержащий это поле, будет отображаться в оглавлении как запись.
builder.Write("MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
builder.Writeln(", will show up in the TOC next to the entry for the above caption.");

// Последовательность этого поля SEQ не соответствует свойству "TableOfFiguresLabel" оглавления,
// и находится в пределах закладки. Его абзац не будет отображаться в оглавлении как запись.
builder.Write("MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "OtherSequence";
builder.Writeln(", will not show up in the TOC because it's from a different sequence identifier.");

// Последовательность этого поля SEQ соответствует свойству TableOfFiguresLabel оглавления и находится в пределах закладки.
// Это поле также ссылается на другую закладку. Содержимое этой закладки появится в записи TOC для этого поля SEQ.
// Само поле SEQ не будет отображать содержимое этой закладки.
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.BookmarkName = "SEQBookmark";
Assert.AreEqual(" SEQ  MySequence SEQBookmark", fieldSeq.GetFieldCode());

// Создать закладку с содержимым, которое будет отображаться в записи оглавления из-за того, что указанное выше поле SEQ ссылается на нее.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark("SEQBookmark");
builder.Write("MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
builder.Writeln(", text from inside SEQBookmark.");
builder.EndBookmark("SEQBookmark");

builder.EndBookmark("TOCBookmark");

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.SEQ.Bookmark.docx");
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
