---
title: PdfSaveOptions.TextCompression
linktitle: TextCompression
articleTitle: TextCompression
second_title: Aspose.Words für .NET
description: Entdecken Sie die TextCompression-Eigenschaft von PdfSaveOptions zur Optimierung Ihrer Dokumente. Wählen Sie den besten Komprimierungstyp für effiziente Textspeicherung und schnelleres Laden.
type: docs
weight: 310
url: /de/net/aspose.words.saving/pdfsaveoptions/textcompression/
---
## PdfSaveOptions.TextCompression property

Gibt den Komprimierungstyp an, der für den gesamten Textinhalt im Dokument verwendet werden soll.

```csharp
public PdfTextCompression TextCompression { get; set; }
```

## Bemerkungen

Standard istFlate.

Erhöht die Ausgabegröße erheblich, wenn ein Dokument ohne Komprimierung gespeichert wird.

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

* enum [PdfTextCompression](../../pdftextcompression/)
* class [PdfSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
