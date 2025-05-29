---
title: PdfSaveOptions.ExportParagraphGraphicsToArtifact
linktitle: ExportParagraphGraphicsToArtifact
articleTitle: ExportParagraphGraphicsToArtifact
second_title: Aspose.Words для .NET
description: Откройте для себя свойство PdfSaveOptions ExportParagraphGraphicsToArtifact для управления графикой абзацев как артефактами, повышая визуальную четкость документа.
type: docs
weight: 160
url: /ru/net/aspose.words.saving/pdfsaveoptions/exportparagraphgraphicstoartifact/
---
## PdfSaveOptions.ExportParagraphGraphicsToArtifact property

Возвращает или задает значение, определяющее, следует ли помечать графический элемент абзаца как артефакт.

```csharp
public bool ExportParagraphGraphicsToArtifact { get; set; }
```

## Примечания

Значение по умолчанию:`ЛОЖЬ` и графика абзаца (подчеркивания, выделение текста и т. д.) будет помечена как «Span» в логической структуре документа.

Когда значение равно`истинный` графика абзаца будет помечена как «Артефакт».

Это значение игнорируется, когда[`ExportDocumentStructure`](../exportdocumentstructure/) является`ЛОЖЬ` .

## Примеры

Показывает, как экспортировать графику абзаца как артефакт (подчеркивания, выделение текста и т. д.).

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
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
