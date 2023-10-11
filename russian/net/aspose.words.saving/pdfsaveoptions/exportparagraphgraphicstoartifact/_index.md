---
title: PdfSaveOptions.ExportParagraphGraphicsToArtifact
second_title: Справочник по API Aspose.Words для .NET
description: PdfSaveOptions свойство. Получает или задает значение определяющее следует ли помечать изображение абзаца как артефакт.
type: docs
weight: 160
url: /ru/net/aspose.words.saving/pdfsaveoptions/exportparagraphgraphicstoartifact/
---
## PdfSaveOptions.ExportParagraphGraphicsToArtifact property

Получает или задает значение, определяющее, следует ли помечать изображение абзаца как артефакт.

```csharp
public bool ExportParagraphGraphicsToArtifact { get; set; }
```

### Примечания

Значение по умолчанию:`ЛОЖЬ` а графика абзаца (подчеркивание, выделение текста и т. д.) будет помечена как «Span» в логической структуре документа.

Когда значение`истинный` графика абзаца будет помечена как «Артефакт».

Это значение игнорируется, если[`ExportDocumentStructure`](../exportdocumentstructure/) является`ЛОЖЬ` .

### Примеры

Показывает, как экспортировать графику абзаца в качестве артефакта (подчеркивания, выделения текста и т. д.).

```csharp
Document doc = new Document(MyDir + "PDF artifacts.docx");

PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.ExportDocumentStructure = true;
saveOptions.ExportParagraphGraphicsToArtifact = true;
saveOptions.TextCompression = PdfTextCompression.None;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExportParagraphGraphicsToArtifact.pdf", saveOptions);
```

### Смотрите также

* class [PdfSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../pdfsaveoptions/)
* сборка [Aspose.Words](../../../)


