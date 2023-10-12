---
title: OutlineOptions.CreateOutlinesForHeadingsInTables
second_title: Справочник по API Aspose.Words для .NET
description: OutlineOptions свойство. Указывает создавать ли структуры для заголовков абзацев отформатированных с использованием стилей заголовков внутри таблиц.
type: docs
weight: 40
url: /ru/net/aspose.words.saving/outlineoptions/createoutlinesforheadingsintables/
---
## OutlineOptions.CreateOutlinesForHeadingsInTables property

Указывает, создавать ли структуры для заголовков (абзацев, отформатированных с использованием стилей заголовков) внутри таблиц.

```csharp
public bool CreateOutlinesForHeadingsInTables { get; set; }
```

### Примечания

Значение по умолчанию:`ЛОЖЬ`.

### Примеры

Показывает, как создавать записи схемы PDF-документа для заголовков внутри таблиц.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Создаём таблицу из трёх строк. Первый ряд,
// текст которого мы отформатируем в стиле заголовка, будет служить заголовком столбца.
builder.StartTable();
builder.InsertCell();
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Write("Customers");
builder.EndRow();
builder.InsertCell();
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Normal;
builder.Write("John Doe");
builder.EndRow();
builder.InsertCell();
builder.Write("Jane Doe");
builder.EndTable();

// Создаем объект «PdfSaveOptions», который мы можем передать методу «Save» документа.
// чтобы изменить способ преобразования этого метода в .PDF.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();

// Выходной PDF-документ будет содержать структуру, представляющую собой оглавление со списком заголовков в теле документа.
// Нажатие на запись в этом контуре приведет нас к местоположению соответствующего заголовка.
// Установите для свойства "HeadingsOutlineLevels" значение "1", чтобы получить контур
// для регистрации только заголовков с уровнем заголовка не выше 1.
pdfSaveOptions.OutlineOptions.HeadingsOutlineLevels = 1;

// Установите для свойства CreateOutlinesForHeadingsInTables значение «false», чтобы исключить все заголовки в таблицах,
// такой как тот, который мы создали выше из контура.
// Установите для свойства CreateOutlinesForHeadingsInTables значение «true», чтобы включить все заголовки в таблицы
// в структуре при условии, что они имеют уровень заголовка, не превышающий значение свойства "HeadingsOutlineLevels".
pdfSaveOptions.OutlineOptions.CreateOutlinesForHeadingsInTables = createOutlinesForHeadingsInTables;

doc.Save(ArtifactsDir + "PdfSaveOptions.TableHeadingOutlines.pdf", pdfSaveOptions);
```

### Смотрите также

* class [OutlineOptions](../)
* пространство имен [Aspose.Words.Saving](../../outlineoptions/)
* сборка [Aspose.Words](../../../)


