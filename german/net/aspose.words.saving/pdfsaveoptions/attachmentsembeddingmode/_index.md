---
title: PdfSaveOptions.AttachmentsEmbeddingMode
linktitle: AttachmentsEmbeddingMode
articleTitle: AttachmentsEmbeddingMode
second_title: Aspose.Words für .NET
description: Passen Sie mit PdfSaveOptions die Einbettung von Anhängen in PDFs an. Sorgen Sie für nahtlose Integration und optimierte Dokumentenfreigabe.
type: docs
weight: 30
url: /de/net/aspose.words.saving/pdfsaveoptions/attachmentsembeddingmode/
---
## PdfSaveOptions.AttachmentsEmbeddingMode property

Ruft einen Wert ab oder legt einen Wert fest, der bestimmt, wie Anhänge in das PDF-Dokument eingebettet werden.

```csharp
public PdfAttachmentsEmbeddingMode AttachmentsEmbeddingMode { get; set; }
```

## Bemerkungen

Der Standardwert istNone und Anhänge sind nicht eingebettet.

Die Standards PDF/A-1, PDF/A-2 und reguläres PDF/A-4 (nicht PDF/A-4f) erlauben keine eingebetteten Dateien. None Wert wird automatisch verwendet.

## Beispiele

Zeigt, wie dem PDF-Dokument eingebettete Anhänge hinzugefügt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", "Excel.Sheet", false, true, null);

PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.AttachmentsEmbeddingMode = PdfAttachmentsEmbeddingMode.Annotations;

doc.Save(ArtifactsDir + "PdfSaveOptions.PdfEmbedAttachments.pdf", saveOptions);
```

### Siehe auch

* enum [PdfAttachmentsEmbeddingMode](../../pdfattachmentsembeddingmode/)
* class [PdfSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
