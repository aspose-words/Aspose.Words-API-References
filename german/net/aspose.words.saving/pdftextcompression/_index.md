---
title: PdfTextCompression Enum
linktitle: PdfTextCompression
articleTitle: PdfTextCompression
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aufzählung Aspose.Words.PdfTextCompression für eine effiziente Komprimierung von PDF-Inhalten, die Dateigröße und Leistung verbessert und gleichzeitig die Qualität erhält.
type: docs
weight: 6330
url: /de/net/aspose.words.saving/pdftextcompression/
---
## PdfTextCompression enumeration

Gibt eine Komprimierungsart an, die auf alle Inhalte der PDF-Datei außer Bildern angewendet wird.

```csharp
public enum PdfTextCompression
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| None | `0` | Keine Komprimierung. |
| Flate | `1` | Flate (ZIP)-Komprimierung. |

## Beispiele

Zeigt, wie beim Speichern eines Dokuments im PDF-Format eine Textkomprimierung angewendet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

for (int i = 0; i < 100; i++)
    builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                    "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// Erstellen Sie ein "PdfSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions options = new PdfSaveOptions();

// Setzen Sie die Eigenschaft „TextCompression“ auf „PdfTextCompression.None“, um keine
// Komprimierung auf Text, wenn wir das Dokument als PDF speichern.
// Setzen Sie die Eigenschaft „TextCompression“ auf „PdfTextCompression.Flate“, um die ZIP-Komprimierung anzuwenden
// in Text, wenn wir das Dokument als PDF speichern. Je größer das Dokument, desto größer sind die Auswirkungen.
options.TextCompression = pdfTextCompression;

doc.Save(ArtifactsDir + "PdfSaveOptions.TextCompression.pdf", options);
```

### Siehe auch

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)
