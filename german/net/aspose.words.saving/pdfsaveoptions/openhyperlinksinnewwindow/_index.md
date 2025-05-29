---
title: PdfSaveOptions.OpenHyperlinksInNewWindow
linktitle: OpenHyperlinksInNewWindow
articleTitle: OpenHyperlinksInNewWindow
second_title: Aspose.Words für .NET
description: Steuern Sie das Hyperlink-Verhalten in Ihrer PDF-Datei mit PdfSaveOptions. Richten Sie Links einfach so ein, dass sie in einem neuen Fenster oder Tab geöffnet werden – für ein verbessertes Benutzererlebnis.
type: docs
weight: 230
url: /de/net/aspose.words.saving/pdfsaveoptions/openhyperlinksinnewwindow/
---
## PdfSaveOptions.OpenHyperlinksInNewWindow property

Ruft einen Wert ab oder legt einen Wert fest, der bestimmt, ob Hyperlinks im PDF-Ausgabedokument in einem neuen Fenster (oder Tab) eines Browsers geöffnet werden müssen.

```csharp
public bool OpenHyperlinksInNewWindow { get; set; }
```

## Bemerkungen

Der Standardwert ist`FALSCH` Wenn dieser Wert auf`WAHR` Hyperlinks werden mit JavaScript-Code gespeichert. JavaScript-Code ist`app.launchURL("URL", true);` , wobei`URL` ist ein Hyperlink.

Beachten Sie, dass, wenn diese Option auf`WAHR` Hyperlinks funktionieren in einigen PDF-Readern, z. B. Chrome, Firefox, nicht

JavaScript-Aktionen sind durch die PDF/A-1- und PDF/A-2-Konformität verboten.`FALSCH`wird automatisch beim Speichern in PDF/A-1 und PDF/A-2 verwendet.

## Beispiele

Zeigt, wie Hyperlinks in einem Dokument gespeichert werden, das wir in PDF konvertieren, sodass beim Anklicken neue Seiten geöffnet werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertHyperlink("Testlink", @"https://www.google.com/search?q=%20aspose", false);

// Erstellen Sie ein "PdfSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions options = new PdfSaveOptions();

// Setzen Sie die Eigenschaft „OpenHyperlinksInNewWindow“ auf „true“, um alle Hyperlinks mithilfe von Javascript-Code zu speichern
// das zwingt die Leser, diese Links in neuen Fenstern/Browser-Tabs zu öffnen.
// Setzen Sie die Eigenschaft „OpenHyperlinksInNewWindow“ auf „false“, um alle Hyperlinks normal zu speichern.
options.OpenHyperlinksInNewWindow = openHyperlinksInNewWindow;

doc.Save(ArtifactsDir + "PdfSaveOptions.OpenHyperlinksInNewWindow.pdf", options);
```

### Siehe auch

* class [PdfSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
