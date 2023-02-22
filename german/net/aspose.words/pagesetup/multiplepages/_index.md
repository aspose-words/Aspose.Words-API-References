---
title: PageSetup.MultiplePages
second_title: Aspose.Words für .NET-API-Referenz
description: PageSetup eigendom. Ruft bei mehrseitigen Dokumenten ab oder legt fest wie ein Dokument gedruckt oder wiedergegeben wird damit es als Broschüre gebunden werden kann.
type: docs
weight: 260
url: /de/net/aspose.words/pagesetup/multiplepages/
---
## PageSetup.MultiplePages property

Ruft bei mehrseitigen Dokumenten ab oder legt fest, wie ein Dokument gedruckt oder wiedergegeben wird, damit es als Broschüre gebunden werden kann.

```csharp
public MultiplePagesType MultiplePages { get; set; }
```

### Beispiele

Zeigt, wie ein Dokument konfiguriert wird, das als Buchfalz gedruckt werden kann.

```csharp
Document doc = new Document();

// Text einfügen, der 16 Seiten umfasst.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("My Booklet:");

for (int i = 0; i < 15; i++)
{
    builder.InsertBreak(BreakType.PageBreak);
    builder.Write($"Booklet face #{i}");
}

// Konfigurieren Sie die "PageSetup"-Eigenschaft des ersten Abschnitts, um das Dokument in Form einer Buchfaltung zu drucken.
// Wenn wir dieses Dokument auf beiden Seiten drucken, können wir die Seiten nehmen, um sie zu stapeln
// und alle auf einmal in der Mitte falten. Der Inhalt des Dokuments wird in einer Buchfalte ausgerichtet.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;

// Wir können die Anzahl der Blätter nur in Vielfachen von 4 angeben.
pageSetup.SheetsPerBooklet = 4;

doc.Save(ArtifactsDir + "PageSetup.Booklet.docx");
```

Zeigt, wie Bundränder festgelegt werden.

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

// Ein Bundsteg fügt entweder dem linken oder rechten Seitenrand Leerzeichen hinzu,
// was das mittige Falten von Seiten in einem Buch ausgleicht, das in das Layout der Seite eingreift.
PageSetup pageSetup = doc.Sections[0].PageSetup;

 // Bestimmen Sie, wie viel Platz unsere Seiten für Text innerhalb der Ränder haben, und fügen Sie dann einen Betrag hinzu, um einen Rand aufzufüllen.
Assert.AreEqual(470.30d, pageSetup.PageWidth - pageSetup.LeftMargin - pageSetup.RightMargin, 0.01d);

pageSetup.Gutter = 100.0d;

// Setzen Sie die Eigenschaft "RtlGutter" auf "true", um den Bundsteg an einer geeigneteren Position für von rechts nach links verlaufenden Text zu platzieren.
pageSetup.RtlGutter = true;

// Legen Sie die Eigenschaft "MultiplePages" auf "MultiplePagesType.MirrorMargins" fest, um zu wechseln
// die linke/rechte Seitenposition der Ränder jeder Seite.
pageSetup.MultiplePages = MultiplePagesType.MirrorMargins;

doc.Save(ArtifactsDir + "PageSetup.Gutter.docx");
```

### Siehe auch

* enum [MultiplePagesType](../../../aspose.words.settings/multiplepagestype/)
* class [PageSetup](../)
* namensraum [Aspose.Words](../../pagesetup/)
* Montage [Aspose.Words](../../../)


