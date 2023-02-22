---
title: PdfSaveOptions.PageMode
second_title: Справочник по API Aspose.Words для .NET
description: PdfSaveOptions свойство. Указывает как документ PDF должен отображаться при открытии в программе чтения PDF.
type: docs
weight: 220
url: /ru/net/aspose.words.saving/pdfsaveoptions/pagemode/
---
## PdfSaveOptions.PageMode property

Указывает, как документ PDF должен отображаться при открытии в программе чтения PDF.

```csharp
public PdfPageMode PageMode { get; set; }
```

### Примечания

Значение по умолчанию:UseOutlines .

### Примеры

Показывает, как установить инструкции для некоторых программ чтения PDF, которым следует следовать при открытии выходного документа.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Создаем объект "PdfSaveOptions", который мы можем передать в метод "Сохранить" документа
// для изменения того, как этот метод преобразует документ в .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Установите для свойства "PageMode" значение "PdfPageMode.FullScreen", чтобы средство чтения PDF открывало сохраненный
// документ в полноэкранном режиме, который занимает дисплей монитора и не имеет видимых элементов управления.
// Установите для свойства "PageMode" значение "PdfPageMode.UseThumbs", чтобы средство чтения PDF отображало отдельную панель
// с миниатюрой для каждой страницы документа.
// Установите для свойства "PageMode" значение "PdfPageMode.UseOC", чтобы средство чтения PDF отображало отдельную панель
// что позволяет нам работать с любыми слоями, присутствующими в документе.
// Установите для свойства "PageMode" значение "PdfPageMode.UseOutlines", чтобы получить программу для чтения PDF
// также для отображения контура, если это возможно.
// Установите для свойства "PageMode" значение "PdfPageMode.UseNone", чтобы средство чтения PDF отображало только сам документ.
// Установите для свойства "PageMode" значение "PdfPageMode.UseAttachments", чтобы панель вложений стала видимой.
options.PageMode = pageMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.PageMode.pdf", options);
```

Показывает, как обрабатывать закладки в верхних/нижних колонтитулах в документе, который мы преобразуем в PDF.

```csharp
Document doc = new Document(MyDir + "Bookmarks in headers and footers.docx");

// Создаем объект "PdfSaveOptions", который мы можем передать в метод "Сохранить" документа
// для изменения того, как этот метод преобразует документ в .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Установите для свойства "PageMode" значение "PdfPageMode.UseOutlines", чтобы отобразить панель навигации схемы в выходном PDF-файле.
saveOptions.PageMode = PdfPageMode.UseOutlines;

// Установите для свойства "DefaultBookmarksOutlineLevel" значение "1", чтобы отобразить все
// закладки на первом уровне схемы в выходном PDF.
saveOptions.OutlineOptions.DefaultBookmarksOutlineLevel = 1;

// Установите для свойства "HeaderFooterBookmarksExportMode" значение "HeaderFooterBookmarksExportMode.None", чтобы
// не экспортировать закладки внутри верхних/нижних колонтитулов.
// Установите для свойства "HeaderFooterBookmarksExportMode" значение "HeaderFooterBookmarksExportMode.First", чтобы
// экспортировать закладки только в верхний/нижний колонтитулы первого раздела.
// Установите для свойства "HeaderFooterBookmarksExportMode" значение "HeaderFooterBookmarksExportMode.All", чтобы
// экспортировать закладки, которые есть во всех верхних/нижних колонтитулах.
saveOptions.HeaderFooterBookmarksExportMode = headerFooterBookmarksExportMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.HeaderFooterBookmarksExportMode.pdf", saveOptions);
```

### Смотрите также

* enum [PdfPageMode](../../pdfpagemode/)
* class [PdfSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../pdfsaveoptions/)
* сборка [Aspose.Words](../../../)


