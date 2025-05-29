---
title: PdfSaveOptions.DisplayDocTitle
linktitle: DisplayDocTitle
articleTitle: DisplayDocTitle
second_title: Aspose.Words для .NET
description: Узнайте, как свойство PdfSaveOptions DisplayDocTitle улучшает работу с PDF-файлами, отображая заголовки документов в строке заголовка Windows для легкой идентификации.
type: docs
weight: 90
url: /ru/net/aspose.words.saving/pdfsaveoptions/displaydoctitle/
---
## PdfSaveOptions.DisplayDocTitle property

Флаг, указывающий, должно ли в строке заголовка окна отображаться название документа, взятое из записи «Название» словаря информации о документе.

```csharp
public bool DisplayDocTitle { get; set; }
```

## Примечания

Если`ЛОЖЬ`, в строке заголовка вместо этого должно отображаться имя PDF-файла, содержащего документ.

Этот флаг необходим для соответствия требованиям PDF/UA.`истинный` значение будет использовано автоматически при сохранении в PDF/UA.

Значение по умолчанию:`ЛОЖЬ`.

## Примеры

Показывает, как отобразить заголовок документа в строке заголовка.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

doc.BuiltInDocumentProperties.Title = "Windows bar pdf title";

// Создаем объект "PdfSaveOptions", который можно передать методу "Save" документа
// чтобы изменить способ преобразования этим методом документа в .PDF.
// Установите "DisplayDocTitle" на "true", чтобы получить доступ к некоторым программам для чтения PDF-файлов, таким как Adobe Acrobat Pro,
// для отображения значения встроенного свойства документа «Заголовок» на вкладке, принадлежащей этому документу.
// Установите "DisplayDocTitle" на "false", чтобы заставить такие считыватели отображать имя файла документа.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions { DisplayDocTitle = displayDocTitle };

doc.Save(ArtifactsDir + "PdfSaveOptions.DocTitle.pdf", pdfSaveOptions);
```

### Смотрите также

* class [PdfSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
