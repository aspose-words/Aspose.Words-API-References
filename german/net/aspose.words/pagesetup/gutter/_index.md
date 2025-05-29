---
title: PageSetup.Gutter
linktitle: Gutter
articleTitle: Gutter
second_title: Aspose.Words für .NET
description: Passen Sie die Seiteneinstellungen für den Bundsteg an, um die Dokumentränder für die Bindung zu optimieren. Verbessern Sie Ihr Layout mit perfekten Rändern für professionelle Ergebnisse.
type: docs
weight: 160
url: /de/net/aspose.words/pagesetup/gutter/
---
## PageSetup.Gutter property

Ruft den zusätzlichen Platz ab, der zum Rand für die Dokumentbindung hinzugefügt wird, oder legt diesen fest.

```csharp
public double Gutter { get; set; }
```

## Beispiele

Zeigt, wie ein Dokument konfiguriert wird, das als Buchfalz gedruckt werden kann.

```csharp
Document doc = new Document();

// Text einfügen, der sich über 16 Seiten erstreckt.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("My Booklet:");

for (int i = 0; i < 15; i++)
{
    builder.InsertBreak(BreakType.PageBreak);
    builder.Write($"Booklet face #{i}");
}

// Konfigurieren Sie die Eigenschaft „PageSetup“ des ersten Abschnitts, um das Dokument in Form einer Buchfalte zu drucken.
// Wenn wir dieses Dokument beidseitig drucken, können wir die Seiten nehmen, um sie zu stapeln
// und falten Sie sie alle gleichzeitig in der Mitte. Der Inhalt des Dokuments wird in einer Buchfalte ausgerichtet.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;

// Wir können die Anzahl der Blätter nur in Vielfachen von 4 angeben.
pageSetup.SheetsPerBooklet = 4;

doc.Save(ArtifactsDir + "PageSetup.Booklet.docx");
```

Zeigt, wie Bundstege eingestellt werden.

```csharp
Document doc = new Document();

// Text einfügen, der sich über mehrere Seiten erstreckt.
DocumentBuilder builder = new DocumentBuilder(doc);
for (int i = 0; i < 6; i++)
{
    builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                  "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
    builder.InsertBreak(BreakType.PageBreak);
}

// Ein Rand fügt Leerzeichen entweder am linken oder rechten Seitenrand hinzu,
// wodurch das Falten der Seiten in der Mitte eines Buches ausgeglichen wird, wodurch das Seitenlayout beeinträchtigt wird.
PageSetup pageSetup = doc.Sections[0].PageSetup;

    // Bestimmen Sie, wie viel Platz unsere Seiten für Text innerhalb der Ränder haben, und fügen Sie dann einen Betrag hinzu, um einen Rand aufzufüllen.
Assert.AreEqual(470.30d, pageSetup.PageWidth - pageSetup.LeftMargin - pageSetup.RightMargin, 0.01d);

pageSetup.Gutter = 100.0d;

// Setzen Sie die Eigenschaft „RtlGutter“ auf „true“, um den Rand für von rechts nach links verlaufenden Text an einer geeigneteren Position zu platzieren.
pageSetup.RtlGutter = true;

// Setzen Sie die Eigenschaft "MultiplePages" auf "MultiplePagesType.MirrorMargins", um zu wechseln
// die linke/rechte Seitenposition der Ränder jeder Seite.
pageSetup.MultiplePages = MultiplePagesType.MirrorMargins;

doc.Save(ArtifactsDir + "PageSetup.Gutter.docx");
```

### Siehe auch

* class [PageSetup](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
