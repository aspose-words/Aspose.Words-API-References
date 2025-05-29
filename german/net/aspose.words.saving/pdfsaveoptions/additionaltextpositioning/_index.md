---
title: PdfSaveOptions.AdditionalTextPositioning
linktitle: AdditionalTextPositioning
articleTitle: AdditionalTextPositioning
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „AdditionalTextPositioning“ von PdfSaveOptions zur Steuerung der Textpositionierung in PDF-Dateien. Verbessern Sie mühelos das Layout Ihres Dokuments!
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

Wenn`WAHR` werden zusätzliche Textpositionierungsoperatoren in das Ausgabe-PDF geschrieben. Dies kann dazu beitragen, Probleme mit der ungenauen Textpositionierung bei einigen Druckern zu beheben. Der Nachteil ist die größere PDF-Dateigröße.

Der Standardwert ist`FALSCH`.

## Beispiele

Zeigen Sie, wie zusätzliche Textpositionierungsoperatoren geschrieben werden.

```csharp
Document doc = new Document(MyDir + "Text positioning operators.docx");

// Erstellen Sie ein "PdfSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions saveOptions = new PdfSaveOptions
{
    TextCompression = PdfTextCompression.None,

    // Setzen Sie die Eigenschaft "AdditionalTextPositioning" auf "true", um zu versuchen, falsche
    // Elementpositionierung im Ausgabe-PDF, falls vorhanden, auf Kosten einer größeren Dateigröße.
    // Setzen Sie die Eigenschaft „AdditionalTextPositioning“ auf „false“, um das Dokument wie gewohnt zu rendern.
    AdditionalTextPositioning = applyAdditionalTextPositioning
};

doc.Save(ArtifactsDir + "PdfSaveOptions.AdditionalTextPositioning.pdf", saveOptions);
```

### Siehe auch

* class [PdfSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
