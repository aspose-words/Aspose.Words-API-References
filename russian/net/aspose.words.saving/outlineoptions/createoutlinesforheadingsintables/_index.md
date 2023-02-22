---
title: OutlineOptions.CreateOutlinesForHeadingsInTables
second_title: Справочник по API Aspose.Words для .NET
description: OutlineOptions свойство. Указывает создавать ли контуры для заголовков абзацев отформатированных с помощью стилей заголовков внутри таблиц.
type: docs
weight: 40
url: /ru/net/aspose.words.saving/outlineoptions/createoutlinesforheadingsintables/
---
## OutlineOptions.CreateOutlinesForHeadingsInTables property

Указывает, создавать ли контуры для заголовков (абзацев, отформатированных с помощью стилей заголовков) внутри таблиц.

```csharp
public bool CreateOutlinesForHeadingsInTables { get; set; }
```

### Примечания

Значение по умолчанию **ЛОЖЬ**.

### Примеры

Показывает, как создавать записи структуры документа PDF для заголовков внутри таблиц.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Создаем таблицу с тремя строками. Первый ряд,
// чей текст мы оформим в заголовочном стиле, будет служить заголовком столбца.
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

// Создаем объект "PdfSaveOptions", который мы можем передать в метод "Сохранить" документа
// для изменения того, как этот метод преобразует документ в .PDF.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();

// Выходной PDF-документ будет содержать структуру, которая представляет собой оглавление, в котором перечислены заголовки в теле документа.
// Нажав на запись в этой схеме, мы перейдем к расположению соответствующего заголовка.
// Установите для свойства "HeadingsOutlineLevels" значение "1", чтобы получить схему
// регистрировать только заголовки с уровнями заголовков не выше 1.
pdfSaveOptions.OutlineOptions.HeadingsOutlineLevels = 1;

// Установите для свойства "CreateOutlinesForHeadingsInTables" значение "false", чтобы исключить все заголовки в таблицах,
// такой, как тот, который мы создали выше из схемы.
// Установите для свойства "CreateOutlinesForHeadingsInTables" значение "true", чтобы включить все заголовки в таблицах
// в структуре при условии, что у них уровень заголовков не больше значения свойства "HeadingsOutlineLevels".
pdfSaveOptions.OutlineOptions.CreateOutlinesForHeadingsInTables = createOutlinesForHeadingsInTables;

doc.Save(ArtifactsDir + "PdfSaveOptions.TableHeadingOutlines.pdf", pdfSaveOptions);
```

### Смотрите также

* class [OutlineOptions](../)
* пространство имен [Aspose.Words.Saving](../../outlineoptions/)
* сборка [Aspose.Words](../../../)


