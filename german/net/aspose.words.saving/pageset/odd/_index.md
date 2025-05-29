---
title: PageSet.Odd
linktitle: Odd
articleTitle: Odd
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „PageSet Odd“, um für eine effiziente Dokumentenverwaltung ganz einfach alle ungeraden Seiten Ihres Dokuments in ihrer ursprünglichen Reihenfolge abzurufen.
type: docs
weight: 40
url: /de/net/aspose.words.saving/pageset/odd/
---
## PageSet.Odd property

Ruft einen Satz mit allen ungeraden Seiten des Dokuments in ihrer ursprünglichen Reihenfolge ab.

```csharp
public static PageSet Odd { get; }
```

## Bemerkungen

Ungerade Seiten haben gerade Indizes, da Seitenindizes nullbasiert sind.

## Beispiele

Zeigt, wie ungerade Seiten aus dem Dokument exportiert werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

for (int i = 0; i < 5; i++)
{
    builder.Writeln($"Page {i + 1} ({(i % 2 == 0 ? "odd" : "even")})");
    if (i < 4)
        builder.InsertBreak(BreakType.PageBreak);
}

// Erstellen Sie ein "PdfSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions options = new PdfSaveOptions();

// Unten sind drei PageSet-Eigenschaften aufgeführt, die wir verwenden können, um eine Reihe von Seiten herauszufiltern aus
// unser Dokument, das basierend auf der Parität seiner Seitenzahlen in einem Ausgabe-PDF-Dokument gespeichert werden soll.
// 1 - Nur die geraden Seitennummern speichern:
options.PageSet = PageSet.Even;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExportPageSet.Even.pdf", options);

// 2 - Nur die Seiten mit ungeraden Nummern speichern:
options.PageSet = PageSet.Odd;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExportPageSet.Odd.pdf", options);

// 3 - Jede Seite speichern:
options.PageSet = PageSet.All;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExportPageSet.All.pdf", options);
```

### Siehe auch

* class [PageSet](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
