---
title: PageSet.All
linktitle: All
articleTitle: All
second_title: Aspose.Words für .NET
description: Mit der Funktion „PageSet All“ können Sie auf alle Dokumentseiten in ihrer ursprünglichen Reihenfolge zugreifen. Optimieren Sie Ihren Workflow und verbessern Sie mühelos Ihr Dokumentenmanagement!
type: docs
weight: 20
url: /de/net/aspose.words.saving/pageset/all/
---
## PageSet.All property

Ruft einen Satz mit allen Seiten des Dokuments in ihrer ursprünglichen Reihenfolge ab.

```csharp
public static PageSet All { get; }
```

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
