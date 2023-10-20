---
title: PdfSaveOptions.ExportParagraphGraphicsToArtifact
linktitle: ExportParagraphGraphicsToArtifact
articleTitle: ExportParagraphGraphicsToArtifact
second_title: Aspose.Words für .NET
description: PdfSaveOptions ExportParagraphGraphicsToArtifact eigendom. Ruft einen Wert ab oder legt diesen fest der bestimmt ob eine Absatzgrafik als Artefakt markiert werden soll in C#.
type: docs
weight: 160
url: /de/net/aspose.words.saving/pdfsaveoptions/exportparagraphgraphicstoartifact/
---
## PdfSaveOptions.ExportParagraphGraphicsToArtifact property

Ruft einen Wert ab oder legt diesen fest, der bestimmt, ob eine Absatzgrafik als Artefakt markiert werden soll.

```csharp
public bool ExportParagraphGraphicsToArtifact { get; set; }
```

## Bemerkungen

Der Standardwert ist`FALSCH` und Absatzgrafiken (Unterstreichungen, Texthervorhebung usw.) werden in der logischen Struktur des Dokuments als „Span“ markiert.

Wenn der Wert ist`WAHR` Die Absatzgrafiken werden als „Artefakt“ gekennzeichnet.

Dieser Wert wird ignoriert, wenn[`ExportDocumentStructure`](../exportdocumentstructure/) Ist`FALSCH` .

## Beispiele

Zeigt, wie Absatzgrafiken als Artefakt exportiert werden (Unterstreichungen, Texthervorhebung usw.).

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
