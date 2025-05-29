---
title: PdfSaveOptions.PageLayout
linktitle: PageLayout
articleTitle: PageLayout
second_title: Aspose.Words для .NET
description: Откройте для себя свойство PdfSaveOptions PageLayout, чтобы настроить макет вашего PDF для оптимального просмотра в любой программе для чтения. Улучшите представление вашего документа!
type: docs
weight: 250
url: /ru/net/aspose.words.saving/pdfsaveoptions/pagelayout/
---
## PdfSaveOptions.PageLayout property

Указывает макет страницы, который будет использоваться при открытии документа в программе для чтения PDF-файлов.

```csharp
public PdfPageLayout PageLayout { get; set; }
```

## Примечания

Значение по умолчанию:SinglePage .

## Примеры

Показывает, как отображать страницы при открытии в программе для чтения PDF-файлов.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

// Отображаем страницы по две за раз, нечетные страницы слева.
PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.PageLayout = PdfPageLayout.TwoPageLeft;

doc.Save(ArtifactsDir + "PdfSaveOptions.PageLayout.pdf", saveOptions);
```

### Смотрите также

* enum [PdfPageLayout](../../pdfpagelayout/)
* class [PdfSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
