---
title: PdfSaveOptions.AttachmentsEmbeddingMode
linktitle: AttachmentsEmbeddingMode
articleTitle: AttachmentsEmbeddingMode
second_title: Aspose.Words для .NET
description: Настройте, как вложения будут встраиваться в PDF-файлы с помощью PdfSaveOptions. Обеспечьте бесперебойную интеграцию и оптимизированный обмен документами.
type: docs
weight: 30
url: /ru/net/aspose.words.saving/pdfsaveoptions/attachmentsembeddingmode/
---
## PdfSaveOptions.AttachmentsEmbeddingMode property

Возвращает или задает значение, определяющее, как вложения внедряются в документ PDF.

```csharp
public PdfAttachmentsEmbeddingMode AttachmentsEmbeddingMode { get; set; }
```

## Примечания

Значение по умолчанию:None и вложения не встроены.

Стандарты PDF/A-1, PDF/A-2 и обычные PDF/A-4 (не PDF/A-4f) не допускают встроенных файлов. None значение будет использовано автоматически.

## Примеры

Показывает, как добавлять вложения в PDF-документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", "Excel.Sheet", false, true, null);

PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.AttachmentsEmbeddingMode = PdfAttachmentsEmbeddingMode.Annotations;

doc.Save(ArtifactsDir + "PdfSaveOptions.PdfEmbedAttachments.pdf", saveOptions);
```

### Смотрите также

* enum [PdfAttachmentsEmbeddingMode](../../pdfattachmentsembeddingmode/)
* class [PdfSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
