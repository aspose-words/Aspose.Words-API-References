---
title: PdfSaveOptions.EmbedAttachments
linktitle: EmbedAttachments
articleTitle: EmbedAttachments
second_title: Aspose.Words für .NET
description: PdfSaveOptions EmbedAttachments eigendom. Ruft einen Wert ab oder legt diesen fest der bestimmt ob Anhänge in das PDFDokument eingebettet werden sollen oder nicht in C#.
type: docs
weight: 110
url: /de/net/aspose.words.saving/pdfsaveoptions/embedattachments/
---
## PdfSaveOptions.EmbedAttachments property

Ruft einen Wert ab oder legt diesen fest, der bestimmt, ob Anhänge in das PDF-Dokument eingebettet werden sollen oder nicht.

```csharp
public bool EmbedAttachments { get; set; }
```

## Bemerkungen

Der Standardwert ist`FALSCH`und Anhänge werden nicht eingebettet.

Wenn der Wert ist`WAHR` Anhänge werden in das PDF-Dokument eingebettet.

Das Einbetten von Anhängen wird beim Speichern in PDF/A- und PDF/UA-Konformität nicht unterstützt. `FALSCH` Der Wert wird automatisch verwendet.

Das Einbetten von Anhängen wird nicht unterstützt, wenn die Verschlüsselung aktiviert ist.`FALSCH` value wird automatisch verwendet.

## Beispiele

Zeigt, wie man eingebettete Anhänge zum PDF-Dokument hinzufügt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", "Excel.Sheet", false, true, null);

PdfSaveOptions options = new PdfSaveOptions();
options.EmbedAttachments = true;

doc.Save(ArtifactsDir + "PdfSaveOptions.PdfEmbedAttachments.pdf", options);
```

### Siehe auch

* class [PdfSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
