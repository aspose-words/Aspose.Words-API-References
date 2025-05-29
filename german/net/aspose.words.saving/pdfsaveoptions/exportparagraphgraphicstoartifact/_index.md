---
title: PdfSaveOptions.ExportParagraphGraphicsToArtifact
linktitle: ExportParagraphGraphicsToArtifact
articleTitle: ExportParagraphGraphicsToArtifact
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „PdfSaveOptions ExportParagraphGraphicsToArtifact“, um Absatzgrafiken als Artefakte zu steuern und so die visuelle Klarheit Ihres Dokuments zu verbessern.
type: docs
weight: 160
url: /de/net/aspose.words.saving/pdfsaveoptions/exportparagraphgraphicstoartifact/
---
## PdfSaveOptions.ExportParagraphGraphicsToArtifact property

Ruft einen Wert ab oder legt einen Wert fest, der bestimmt, ob eine Absatzgrafik als Artefakt markiert werden soll.

```csharp
public bool ExportParagraphGraphicsToArtifact { get; set; }
```

## Bemerkungen

Der Standardwert ist`FALSCH` und Absatzgrafiken (Unterstreichungen, Texthervorhebungen usw.) werden in der logischen Struktur des Dokuments als „Span“ gekennzeichnet.

Wenn der Wert`WAHR` die Absatzgrafiken werden als „Artefakt“ gekennzeichnet.

Dieser Wert wird ignoriert, wenn[`ExportDocumentStructure`](../exportdocumentstructure/) Ist`FALSCH` .

## Beispiele

Zeigt, wie Absatzgrafiken als Artefakt (Unterstreichungen, Texthervorhebungen usw.) exportiert werden.

```csharp
Document doc = new Document(MyDir + "PDF artifacts.docx");

PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.ExportDocumentStructure = true;
saveOptions.ExportParagraphGraphicsToArtifact = true;
saveOptions.TextCompression = PdfTextCompression.None;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExportParagraphGraphicsToArtifact.pdf", saveOptions);
```

### Siehe auch

* class [PdfSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
