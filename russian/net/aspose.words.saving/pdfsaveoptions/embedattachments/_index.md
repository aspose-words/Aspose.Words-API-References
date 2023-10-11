---
title: PdfSaveOptions.EmbedAttachments
second_title: Справочник по API Aspose.Words для .NET
description: PdfSaveOptions свойство. Получает или задает значение определяющее следует ли встраивать вложения в PDFдокумент.
type: docs
weight: 110
url: /ru/net/aspose.words.saving/pdfsaveoptions/embedattachments/
---
## PdfSaveOptions.EmbedAttachments property

Получает или задает значение, определяющее, следует ли встраивать вложения в PDF-документ.

```csharp
public bool EmbedAttachments { get; set; }
```

### Примечания

Значение по умолчанию:`ЛОЖЬ`и вложения не встраиваются.

Когда значение`истинный` вложения встраиваются в PDF-документ.

Встраивание вложений не поддерживается при сохранении в формате PDF/A и PDF/UA. `ЛОЖЬ` значение будет использовано автоматически.

Встраивание вложений не поддерживается, если включено шифрование.`ЛОЖЬ` value будет использоваться автоматически.

### Примеры

Показывает, как добавлять вложения в PDF-документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", "Excel.Sheet", false, true, null);

PdfSaveOptions options = new PdfSaveOptions();
options.EmbedAttachments = true;

doc.Save(ArtifactsDir + "PdfSaveOptions.PdfEmbedAttachments.pdf", options);
```

### Смотрите также

* class [PdfSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../pdfsaveoptions/)
* сборка [Aspose.Words](../../../)


