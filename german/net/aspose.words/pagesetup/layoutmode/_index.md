---
title: PageSetup.LayoutMode
second_title: Aspose.Words für .NET-API-Referenz
description: PageSetup eigendom. Ruft den Layoutmodus dieses Abschnitts ab oder legt ihn fest.
type: docs
weight: 190
url: /de/net/aspose.words/pagesetup/layoutmode/
---
## PageSetup.LayoutMode property

Ruft den Layoutmodus dieses Abschnitts ab oder legt ihn fest.

```csharp
public SectionLayoutMode LayoutMode { get; set; }
```

### Beispiele

Zeigt, wie man a für die Anzahl der Zeichen angibt, die jede Zeile haben darf.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aktivieren Sie Pitching und verwenden Sie es dann, um die Anzahl der Zeichen pro Zeile in diesem Abschnitt festzulegen.
builder.PageSetup.LayoutMode = SectionLayoutMode.Grid;
builder.PageSetup.CharactersPerLine = 10;

// Die Anzahl der Zeichen hängt auch von der Schriftgröße ab.
doc.Styles["Normal"].Font.Size = 20;

Assert.AreEqual(8, doc.FirstSection.PageSetup.CharactersPerLine);

builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.Save(ArtifactsDir + "PageSetup.CharactersPerLine.docx");
```

Zeigt, wie Sie ein Limit für die Anzahl der Zeilen angeben, die jede Seite haben darf.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aktivieren Sie Pitching und verwenden Sie es dann, um die Anzahl der Zeilen pro Seite in diesem Abschnitt festzulegen.
// Eine ausreichend große Schriftgröße verschiebt einige Zeilen nach unten auf die nächste Seite, um überlappende Zeichen zu vermeiden.
builder.PageSetup.LayoutMode = SectionLayoutMode.LineGrid;
builder.PageSetup.LinesPerPage = 15;

builder.ParagraphFormat.SnapToGrid = true;

for (int i = 0; i < 30; i++)
    builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");

doc.Save(ArtifactsDir + "PageSetup.LinesPerPage.docx");
```

### Siehe auch

* enum [SectionLayoutMode](../../sectionlayoutmode/)
* class [PageSetup](../)
* namensraum [Aspose.Words](../../pagesetup/)
* Montage [Aspose.Words](../../../)


