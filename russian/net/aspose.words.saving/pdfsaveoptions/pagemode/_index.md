---
title: PdfSaveOptions.PageMode
linktitle: PageMode
articleTitle: PageMode
second_title: Aspose.Words для .NET
description: PdfSaveOptions PageMode свойство. Указывает как PDFдокумент должен отображаться при открытии в программе чтения PDF на С#.
type: docs
weight: 250
url: /ru/net/aspose.words.saving/pdfsaveoptions/pagemode/
---
## PdfSaveOptions.PageMode property

Указывает, как PDF-документ должен отображаться при открытии в программе чтения PDF.

```csharp
public PdfPageMode PageMode { get; set; }
```

## Примечания

Значение по умолчанию:UseOutlines .

## Примеры

Показывает, как установить инструкции для некоторых программ чтения PDF, которым они будут следовать при открытии выходного документа.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Создаем объект «PdfSaveOptions», который мы можем передать методу «Save» документа.
// чтобы изменить способ преобразования этого метода в .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Установите для свойства «PageMode» значение «PdfPageMode.FullScreen», чтобы программа чтения PDF могла открывать сохраненные файлы.
// документ в полноэкранном режиме, который занимает изображение монитора и не имеет видимых элементов управления.
// Установите для свойства «PageMode» значение «PdfPageMode.UseThumbs», чтобы программа чтения PDF отображала отдельную панель.
// с миниатюрой для каждой страницы документа.
// Установите для свойства «PageMode» значение «PdfPageMode.UseOC», чтобы программа чтения PDF отображала отдельную панель.
// что позволяет нам работать с любыми слоями, присутствующими в документе.
// Установите для свойства «PageMode» значение «PdfPageMode.UseOutlines», чтобы получить программу чтения PDF-файлов.
// также для отображения контура, если это возможно.
// Установите для свойства «PageMode» значение «PdfPageMode.UseNone», чтобы программа чтения PDF отображала только сам документ.
// Установите для свойства «PageMode» значение «PdfPageMode.UseAttachments», чтобы сделать панель вложений видимой.
options.PageMode = pageMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.PageMode.pdf", options);
```

Показывает обработку закладок в верхних и нижних колонтитулах документа, который мы преобразуем в PDF.

```csharp
Document doc = new Document(MyDir + "Bookmarks in headers and footers.docx");

// Создаем объект «PdfSaveOptions», который мы можем передать методу «Save» документа.
// чтобы изменить способ преобразования этого метода в .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Установите для свойства «PageMode» значение «PdfPageMode.UseOutlines», чтобы отобразить контурную панель навигации в выходном PDF-файле.
saveOptions.PageMode = PdfPageMode.UseOutlines;

// Установите для свойства «DefaultBookmarksOutlineLevel» значение «1», чтобы отобразить все
// закладки на первом уровне структуры в выходном PDF.
saveOptions.OutlineOptions.DefaultBookmarksOutlineLevel = 1;

// Установите для свойства «HeaderFooterBookmarksExportMode» значение «HeaderFooterBookmarksExportMode.None», чтобы
// не экспортировать закладки, находящиеся внутри верхних/нижних колонтитулов.
// Установите для свойства "HeaderFooterBookmarksExportMode" значение "HeaderFooterBookmarksExportMode.First", чтобы
// экспортируем только закладки в верхнем/нижнем колонтитуле первого раздела.
// Установите для свойства «HeaderFooterBookmarksExportMode» значение «HeaderFooterBookmarksExportMode.All», чтобы
// экспортируем закладки, которые есть во всех верхних/нижних колонтитулах.
saveOptions.HeaderFooterBookmarksExportMode = headerFooterBookmarksExportMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.HeaderFooterBookmarksExportMode.pdf", saveOptions);
```

### Смотрите также

* enum [PdfPageMode](../../pdfpagemode/)
* class [PdfSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
