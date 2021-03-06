---
title: DisplayDocTitle
second_title: Aspose.Words für .NET-API-Referenz
description: Ein Flag das angibt ob die Titelleiste des Fensters den Dokumenttitel anzeigen soll der aus dem Titeleintrag des Dokumentinformationsverzeichnisses stammt.
type: docs
weight: 70
url: /de/net/aspose.words.saving/pdfsaveoptions/displaydoctitle/
---
## PdfSaveOptions.DisplayDocTitle property

Ein Flag, das angibt, ob die Titelleiste des Fensters den Dokumenttitel anzeigen soll, der aus dem Titeleintrag des Dokumentinformationsverzeichnisses stammt.

```csharp
public bool DisplayDocTitle { get; set; }
```

### Bemerkungen

Wenn`FALSCH`, sollte die Titelleiste stattdessen den Namen der PDF-Datei anzeigen, die das Dokument enthält.

Dieses Flag ist für die PDF/UA-Konformität erforderlich.`Stimmt` Der Wert wird automatisch verwendet, wenn in PDF/UA gespeichert wird.

Der Standardwert ist`FALSCH`.

### Beispiele

Zeigt, wie der Titel des Dokuments als Titelleiste angezeigt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

doc.BuiltInDocumentProperties.Title = "Windows bar pdf title";

// Erstellen Sie ein "PdfSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
// Setzen Sie "DisplayDocTitle" auf "true", um einige PDF-Reader wie Adobe Acrobat Pro zu erhalten.
// um den Wert der eingebauten Eigenschaft "Title" des Dokuments in der Registerkarte anzuzeigen, die zu diesem Dokument gehört.
// Setzen Sie "DisplayDocTitle" auf "false", damit solche Reader den Dateinamen des Dokuments anzeigen.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions { DisplayDocTitle = displayDocTitle };

doc.Save(ArtifactsDir + "PdfSaveOptions.DocTitle.pdf", pdfSaveOptions);
```

### Siehe auch

* class [PdfSaveOptions](../../pdfsaveoptions)
* namensraum [Aspose.Words.Saving](../../pdfsaveoptions)
* Montage [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
