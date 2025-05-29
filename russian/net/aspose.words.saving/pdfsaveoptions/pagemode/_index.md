---
title: PdfSaveOptions.PageMode
linktitle: PageMode
articleTitle: PageMode
second_title: Aspose.Words для .NET
description: Узнайте, как свойство PageMode PdfSaveOptions улучшает ваши впечатления от просмотра PDF-файлов, настраивая отображение документа в любой программе для чтения PDF-файлов.
type: docs
weight: 260
url: /ru/net/aspose.words.saving/pdfsaveoptions/pagemode/
---
## PdfSaveOptions.PageMode property

Указывает, как должен отображаться PDF-документ при открытии в программе для чтения PDF-файлов.

```csharp
public PdfPageMode PageMode { get; set; }
```

## Примечания

Значение по умолчанию:UseOutlines .

## Примеры

Показывает, как задать инструкции, которым должны следовать некоторые программы чтения PDF-файлов при открытии выходного документа.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Создаем объект "PdfSaveOptions", который можно передать методу "Save" документа
// чтобы изменить способ преобразования этим методом документа в .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Установите свойство "PageMode" на "PdfPageMode.FullScreen", чтобы программа чтения PDF-файлов открыла сохраненный файл
// документ в полноэкранном режиме, который занимает весь экран монитора и не имеет видимых элементов управления.
// Установите свойство "PageMode" на "PdfPageMode.UseThumbs", чтобы программа чтения PDF-файлов отображала отдельную панель
// с миниатюрой для каждой страницы документа.
// Установите свойство "PageMode" на "PdfPageMode.UseOC", чтобы программа чтения PDF-файлов отображала отдельную панель
// что позволяет нам работать с любыми слоями, присутствующими в документе.
// Установите свойство "PageMode" на "PdfPageMode.UseOutlines", чтобы получить средство чтения PDF-файлов
// также для отображения контура, если это возможно.
// Установите свойство «PageMode» на «PdfPageMode.UseNone», чтобы программа чтения PDF-файлов отображала только сам документ.
// Установите свойство "PageMode" на "PdfPageMode.UseAttachments", чтобы сделать видимой панель вложений.
options.PageMode = pageMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.PageMode.pdf", options);
```

Показывает, как обрабатывать закладки в верхних/нижних колонтитулах документа, который мы преобразуем в PDF.

```csharp
Document doc = new Document(MyDir + "Bookmarks in headers and footers.docx");

// Создаем объект "PdfSaveOptions", который можно передать методу "Save" документа
// чтобы изменить способ преобразования этим методом документа в .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Установите свойство «PageMode» на «PdfPageMode.UseOutlines», чтобы отобразить панель навигации структуры в выходном PDF-файле.
saveOptions.PageMode = PdfPageMode.UseOutlines;

// Установите свойство "DefaultBookmarksOutlineLevel" на "1", чтобы отобразить все
// закладки на первом уровне структуры в выходном PDF-файле.
saveOptions.OutlineOptions.DefaultBookmarksOutlineLevel = 1;

// Установите свойство "HeaderFooterBookmarksExportMode" в значение "HeaderFooterBookmarksExportMode.None" для
// не экспортировать закладки, находящиеся внутри верхних/нижних колонтитулов.
// Установите свойство "HeaderFooterBookmarksExportMode" в значение "HeaderFooterBookmarksExportMode.First" для
// экспортировать закладки только в верхних/нижних колонтитулах первого раздела.
// Установите свойство "HeaderFooterBookmarksExportMode" в значение "HeaderFooterBookmarksExportMode.All" для
// экспортировать закладки, находящиеся во всех верхних/нижних колонтитулах.
saveOptions.HeaderFooterBookmarksExportMode = headerFooterBookmarksExportMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.HeaderFooterBookmarksExportMode.pdf", saveOptions);
```

### Смотрите также

* enum [PdfPageMode](../../pdfpagemode/)
* class [PdfSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
