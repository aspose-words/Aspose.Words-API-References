---
title: OutlineOptions.CreateOutlinesForHeadingsInTables
linktitle: CreateOutlinesForHeadingsInTables
articleTitle: CreateOutlinesForHeadingsInTables
second_title: Aspose.Words для .NET
description: Узнайте, как свойство CreateOutlinesForHeadingsInTables улучшает организацию таблиц, включая контуры для стилей заголовков, повышая ясность документа.
type: docs
weight: 40
url: /ru/net/aspose.words.saving/outlineoptions/createoutlinesforheadingsintables/
---
## OutlineOptions.CreateOutlinesForHeadingsInTables property

Указывает, следует ли создавать контуры для заголовков (абзацев, отформатированных с использованием стилей заголовков) внутри таблиц.

```csharp
public bool CreateOutlinesForHeadingsInTables { get; set; }
```

## Примечания

Значение по умолчанию:`ЛОЖЬ`.

## Примеры

Показывает, как создавать записи структуры PDF-документа для заголовков внутри таблиц.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Создаем таблицу с тремя строками. Первая строка,
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

// Создаем объект "PdfSaveOptions", который можно передать методу "Save" документа
// чтобы изменить способ преобразования этим методом документа в .PDF.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();

// Выходной PDF-документ будет содержать структуру, представляющую собой оглавление, в котором перечислены заголовки в тексте документа.
// Нажатие на запись в этой схеме перенесет нас к местоположению соответствующего заголовка.
// Установите свойство "HeadingsOutlineLevels" на "1", чтобы получить контур
// для регистрации только заголовков с уровнями заголовков не больше 1.
pdfSaveOptions.OutlineOptions.HeadingsOutlineLevels = 1;

// Установите свойство "CreateOutlinesForHeadingsInTables" в значение "false", чтобы исключить все заголовки в таблицах,
// например, тот, который мы создали выше из контура.
// Установите свойство "CreateOutlinesForHeadingsInTables" в значение "true", чтобы включить все заголовки в таблицах
// в структуре, при условии, что их уровень заголовка не превышает значение свойства "HeadingsOutlineLevels".
pdfSaveOptions.OutlineOptions.CreateOutlinesForHeadingsInTables = createOutlinesForHeadingsInTables;

doc.Save(ArtifactsDir + "PdfSaveOptions.TableHeadingOutlines.pdf", pdfSaveOptions);
```

### Смотрите также

* class [OutlineOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
