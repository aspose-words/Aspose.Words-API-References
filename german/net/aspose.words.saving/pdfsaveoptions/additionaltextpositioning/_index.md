---
title: PdfSaveOptions.AdditionalTextPositioning
linktitle: AdditionalTextPositioning
articleTitle: AdditionalTextPositioning
second_title: Aspose.Words für .NET
description: PdfSaveOptions AdditionalTextPositioning eigendom. Ein Flag das angibt ob zusätzliche Textpositionierungsoperatoren geschrieben werden sollen oder nicht in C#.
type: docs
weight: 20
url: /de/net/aspose.words.saving/pdfsaveoptions/additionaltextpositioning/
---
## PdfSaveOptions.AdditionalTextPositioning property

Ein Flag, das angibt, ob zusätzliche Textpositionierungsoperatoren geschrieben werden sollen oder nicht.

```csharp
public bool AdditionalTextPositioning { get; set; }
```

## Bemerkungen

Wenn`WAHR` werden zusätzliche Textpositionierungsoperatoren in das Ausgabe-PDF geschrieben. Dies kann dabei helfen, Probleme mit ungenauer Textpositionierung bei einigen Druckern zu beheben. Der Nachteil ist die größere Größe des PDF-Dokuments.

Der Standardwert ist`FALSCH`.

## Beispiele

Zeigen Sie, wie Sie zusätzliche Textpositionierungsoperatoren schreiben.

```csharp
Document doc = new Document(MyDir + "Text positioning operators.docx");

// Erstellen Sie ein „PdfSaveOptions“-Objekt, das wir an die „Save“-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions saveOptions = new PdfSaveOptions
{
    TextCompression = PdfTextCompression.None,

    // Setzen Sie die Eigenschaft „AdditionalTextPositioning“ auf „true“, um zu versuchen, Fehler zu beheben
    // Elementpositionierung im Ausgabe-PDF, falls vorhanden, auf Kosten einer erhöhten Dateigröße.
    // Setzen Sie die Eigenschaft „AdditionalTextPositioning“ auf „false“, um das Dokument wie gewohnt darzustellen.
    AdditionalTextPositioning = applyAdditionalTextPositioning
};

doc.Save(ArtifactsDir + "PdfSaveOptions.AdditionalTextPositioning.pdf", saveOptions);
```

### Siehe auch

* class [PdfSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
