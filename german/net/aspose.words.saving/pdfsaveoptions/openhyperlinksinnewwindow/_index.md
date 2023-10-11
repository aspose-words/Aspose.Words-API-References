---
title: PdfSaveOptions.OpenHyperlinksInNewWindow
second_title: Aspose.Words für .NET-API-Referenz
description: PdfSaveOptions eigendom. Ruft einen Wert ab oder legt diesen fest der bestimmt ob Hyperlinks im AusgabePDFDokument gezwungen werden in einem neuen Fenster oder Tab eines Browsers geöffnet zu werden.
type: docs
weight: 230
url: /de/net/aspose.words.saving/pdfsaveoptions/openhyperlinksinnewwindow/
---
## PdfSaveOptions.OpenHyperlinksInNewWindow property

Ruft einen Wert ab oder legt diesen fest, der bestimmt, ob Hyperlinks im Ausgabe-PDF-Dokument gezwungen werden, in einem neuen Fenster (oder Tab) eines Browsers geöffnet zu werden.

```csharp
public bool OpenHyperlinksInNewWindow { get; set; }
```

### Bemerkungen

Der Standardwert ist`FALSCH` . Wenn dieser Wert auf eingestellt ist`WAHR` Hyperlinks werden mit JavaScript-Code gespeichert. JavaScript-Code ist`app.launchURL("URL", true);` , wo`URL` ist ein Hyperlink.

Beachten Sie Folgendes: Wenn diese Option auf eingestellt ist`WAHR` Hyperlinks funktionieren in einigen PDF-Readern, z. B. Chrome und Firefox, nicht.

JavaScript-Aktionen sind durch die PDF/A-1- und PDF/A-2-Konformität verboten.`FALSCH`wird automatisch verwendet, wenn in PDF/A-1 und PDF/A-2 gespeichert wird.

### Beispiele

Zeigt, wie man Hyperlinks in einem Dokument speichert, das wir in PDF konvertieren, sodass sie neue Seiten öffnen, wenn wir darauf klicken.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertHyperlink("Testlink", @"https://www.google.com/search?q=%20aspose", false);

// Erstellen Sie ein „PdfSaveOptions“-Objekt, das wir an die „Save“-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions options = new PdfSaveOptions();

// Setzen Sie die Eigenschaft „OpenHyperlinksInNewWindow“ auf „true“, um alle Hyperlinks mit Javascript-Code zu speichern
// das zwingt Leser dazu, diese Links in neuen Fenstern/Browser-Tabs zu öffnen.
// Setzen Sie die Eigenschaft „OpenHyperlinksInNewWindow“ auf „false“, um alle Hyperlinks normal zu speichern.
options.OpenHyperlinksInNewWindow = openHyperlinksInNewWindow;

doc.Save(ArtifactsDir + "PdfSaveOptions.OpenHyperlinksInNewWindow.pdf", options);
```

### Siehe auch

* class [PdfSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../pdfsaveoptions/)
* Montage [Aspose.Words](../../../)


