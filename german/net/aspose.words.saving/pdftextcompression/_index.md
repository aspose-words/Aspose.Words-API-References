---
title: PdfTextCompression Enum
linktitle: PdfTextCompression
articleTitle: PdfTextCompression
second_title: Aspose.Words für .NET
description: Aspose.Words.Saving.PdfTextCompression opsomming. Gibt einen Komprimierungstyp an der auf alle Inhalte in der PDFDatei außer Bildern angewendet wird in C#.
type: docs
weight: 5530
url: /de/net/aspose.words.saving/pdftextcompression/
---
## PdfTextCompression enumeration

Gibt einen Komprimierungstyp an, der auf alle Inhalte in der PDF-Datei außer Bildern angewendet wird.

```csharp
public enum PdfTextCompression
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| None | `0` | Keine Komprimierung. |
| Flate | `1` | Flate (ZIP)-Komprimierung. |

## Beispiele

Zeigt, wie Sie beim Speichern eines Dokuments als PDF eine Textkomprimierung anwenden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

for (int i = 0; i < 100; i++)
    builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                    "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// Erstellen Sie ein „PdfSaveOptions“-Objekt, das wir an die „Save“-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions options = new PdfSaveOptions();

// Setzen Sie die Eigenschaft „TextCompression“ auf „PdfTextCompression.None“, um keine anzuwenden
// Komprimierung in Text, wenn wir das Dokument als PDF speichern.
// Setzen Sie die Eigenschaft „TextCompression“ auf „PdfTextCompression.Flate“, um die ZIP-Komprimierung anzuwenden
// in Text, wenn wir das Dokument als PDF speichern. Je größer das Dokument ist, desto größer sind die Auswirkungen.
options.TextCompression = pdfTextCompression;

doc.Save(ArtifactsDir + "PdfSaveOptions.TextCompression.pdf", options);
```

### Siehe auch

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)
