---
title: FixedPageSaveOptions.PageSet
linktitle: PageSet
articleTitle: PageSet
second_title: Aspose.Words für .NET
description: Steuern Sie die Dokumentdarstellung mit FixedPageSaveOptions PageSet. Wählen Sie einfach einzelne Seiten aus oder wählen Sie alle für eine nahtlose Ausgabe. Optimieren Sie Ihren Workflow!
type: docs
weight: 70
url: /de/net/aspose.words.saving/fixedpagesaveoptions/pageset/
---
## FixedPageSaveOptions.PageSet property

Ruft die zu rendernden Seiten ab oder legt sie fest. Standardmäßig sind alle Seiten im Dokument dargestellt.

```csharp
public PageSet PageSet { get; set; }
```

## Beispiele

Zeigt, wie Seiten basierend auf genauen Seitenindizes extrahiert werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

//Fügen Sie dem Dokument fünf Seiten hinzu.
for (int i = 1; i < 6; i++)
{
    builder.Write("Page " + i);
    builder.InsertBreak(BreakType.PageBreak);
}

// Erstellen Sie ein "XpsSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .XPS konvertiert.
XpsSaveOptions xpsOptions = new XpsSaveOptions();

// Verwenden Sie die Eigenschaft „PageSet“, um einen Satz von Dokumentseiten auszuwählen, die im XPS-Ausgabeformat gespeichert werden sollen.
// In diesem Fall wählen wir über einen nullbasierten Index nur drei Seiten aus: Seite 1, Seite 2 und Seite 4.
xpsOptions.PageSet = new PageSet(0, 1, 3);

doc.Save(ArtifactsDir + "XpsSaveOptions.ExportExactPages.xps", xpsOptions);
```

Zeigt, wie nur einige Seiten eines Dokuments in PDF konvertiert werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

using (Stream stream = File.Create(ArtifactsDir + "PdfSaveOptions.OnePage.pdf"))
{
    // Erstellen Sie ein "PdfSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
    // um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
    PdfSaveOptions options = new PdfSaveOptions();

    // Setzen Sie den „PageIndex“ auf „1“, um einen Teil des Dokuments ab der zweiten Seite zu rendern.
    options.PageSet = new PageSet(1);

    // Dieses Dokument enthält eine Seite ab Seite zwei, die wiederum nur die zweite Seite enthält.
    doc.Save(stream, options);
}
```

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

* class [PageSet](../../pageset/)
* class [FixedPageSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
