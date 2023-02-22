---
title: PdfSaveOptions.OpenHyperlinksInNewWindow
second_title: Aspose.Words für .NET-API-Referenz
description: PdfSaveOptions eigendom. Ruft einen Wert ab oder legt ihn fest der bestimmt ob Hyperlinks im ausgegebenen PDFDokument zwangsweise in einem neuen Fenster oder Tab eines Browsers geöffnet werden.
type: docs
weight: 200
url: /de/net/aspose.words.saving/pdfsaveoptions/openhyperlinksinnewwindow/
---
## PdfSaveOptions.OpenHyperlinksInNewWindow property

Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob Hyperlinks im ausgegebenen PDF-Dokument zwangsweise in einem neuen Fenster (oder Tab) eines Browsers geöffnet werden.

```csharp
public bool OpenHyperlinksInNewWindow { get; set; }
```

### Bemerkungen

Der Standardwert ist`FALSCH` . Wenn dieser Wert auf eingestellt ist`Stimmt` Hyperlinks werden mit JavaScript-Code gespeichert. JavaScript-Code ist`app.launchURL("URL", wahr);`, wo`URL` ist ein Hyperlink.

Beachten Sie, dass wenn diese Option auf eingestellt ist`Stimmt` Hyperlinks funktionieren nicht in einigen PDF-Readern, z. B. Chrome, Firefox.

JavaScript-Aktionen sind durch die PDF/A-1- und PDF/A-2-Konformität verboten.`FALSCH` wird automatisch verwendet, wenn in PDF/A-1 und PDF/A-2 gespeichert wird.

### Beispiele

Zeigt, wie Hyperlinks in einem Dokument gespeichert werden, das wir in PDF konvertieren, sodass sie neue Seiten öffnen, wenn wir darauf klicken.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertHyperlink("Testlink", @"https://www.google.com/search?q=%20aspose", false);

// Erstellen Sie ein "PdfSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions options = new PdfSaveOptions();

// Setzen Sie die Eigenschaft "OpenHyperlinksInNewWindow" auf "true", um alle Hyperlinks mit Javascript-Code zu speichern
// das zwingt die Leser, diese Links in neuen Fenstern/Browser-Tabs zu öffnen.
// Setzen Sie die Eigenschaft "OpenHyperlinksInNewWindow" auf "false", um alle Hyperlinks normal zu speichern.
options.OpenHyperlinksInNewWindow = openHyperlinksInNewWindow;

doc.Save(ArtifactsDir + "PdfSaveOptions.OpenHyperlinksInNewWindow.pdf", options);
```

### Siehe auch

* class [PdfSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../pdfsaveoptions/)
* Montage [Aspose.Words](../../../)


