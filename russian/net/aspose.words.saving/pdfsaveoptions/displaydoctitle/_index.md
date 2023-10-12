---
title: PdfSaveOptions.DisplayDocTitle
second_title: Справочник по API Aspose.Words для .NET
description: PdfSaveOptions свойство. Флаг указывающий должен ли заголовок окна отображать заголовок документа взятый из записи заголовка словаря информации о документе.
type: docs
weight: 80
url: /ru/net/aspose.words.saving/pdfsaveoptions/displaydoctitle/
---
## PdfSaveOptions.DisplayDocTitle property

Флаг, указывающий, должен ли заголовок окна отображать заголовок документа, взятый из записи заголовка словаря информации о документе.

```csharp
public bool DisplayDocTitle { get; set; }
```

### Примечания

Если`ЛОЖЬ`, в строке заголовка вместо этого должно отображаться имя PDF-файла, содержащего документ.

Этот флаг требуется для соответствия PDF/UA.`истинный` значение будет использоваться автоматически при сохранении в PDF/UA.

Значение по умолчанию:`ЛОЖЬ`.

### Примеры

Показывает, как отобразить заголовок документа в строке заголовка.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

doc.BuiltInDocumentProperties.Title = "Windows bar pdf title";

// Создаем объект «PdfSaveOptions», который мы можем передать методу «Save» документа.
// чтобы изменить способ преобразования этого метода в .PDF.
// Установите для параметра «DisplayDocTitle» значение «true», чтобы получить доступ к некоторым программам для чтения PDF-файлов, например Adobe Acrobat Pro,
// для отображения значения встроенного свойства документа «Заголовок» на вкладке, принадлежащей этому документу.
// Установите для параметра «DisplayDocTitle» значение «false», чтобы такие программы чтения могли отображать имя файла документа.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions { DisplayDocTitle = displayDocTitle };

doc.Save(ArtifactsDir + "PdfSaveOptions.DocTitle.pdf", pdfSaveOptions);
```

### Смотрите также

* class [PdfSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../pdfsaveoptions/)
* сборка [Aspose.Words](../../../)


