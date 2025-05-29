---
title: PdfSaveOptions.DisplayDocTitle
linktitle: DisplayDocTitle
articleTitle: DisplayDocTitle
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die DisplayDocTitle-Eigenschaft von PdfSaveOptions Ihr PDF-Erlebnis verbessert, indem Dokumenttitel zur einfachen Identifizierung in der Windows-Titelleiste angezeigt werden.
type: docs
weight: 90
url: /de/net/aspose.words.saving/pdfsaveoptions/displaydoctitle/
---
## PdfSaveOptions.DisplayDocTitle property

Ein Flag, das angibt, ob in der Titelleiste des Fensters der Dokumenttitel angezeigt werden soll, der dem Titeleintrag des Dokumentinformationswörterbuchs entnommen wurde.

```csharp
public bool DisplayDocTitle { get; set; }
```

## Bemerkungen

Wenn`FALSCH`, sollte in der Titelleiste stattdessen der Name der PDF-Datei angezeigt werden, die das Dokument enthält.

Dieses Flag ist für die PDF/UA-Konformität erforderlich.`WAHR` Der Wert wird automatisch verwendet, wenn als PDF/UA gespeichert wird.

Der Standardwert ist`FALSCH`.

## Beispiele

Zeigt, wie der Titel des Dokuments als Titelleiste angezeigt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

doc.BuiltInDocumentProperties.Title = "Windows bar pdf title";

// Erstellen Sie ein "PdfSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
// Setzen Sie den "DisplayDocTitle" auf "true", um einige PDF-Reader wie Adobe Acrobat Pro zu erhalten,
// um den Wert der integrierten Eigenschaft „Titel“ des Dokuments in der Registerkarte anzuzeigen, die zu diesem Dokument gehört.
// Setzen Sie „DisplayDocTitle“ auf „false“, damit solche Reader den Dateinamen des Dokuments anzeigen.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions { DisplayDocTitle = displayDocTitle };

doc.Save(ArtifactsDir + "PdfSaveOptions.DocTitle.pdf", pdfSaveOptions);
```

### Siehe auch

* class [PdfSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
