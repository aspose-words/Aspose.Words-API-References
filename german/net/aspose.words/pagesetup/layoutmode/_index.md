---
title: PageSetup.LayoutMode
linktitle: LayoutMode
articleTitle: LayoutMode
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „PageSetup LayoutMode“, um das Layout Ihres Dokuments einfach anzupassen. Verbessern Sie Ihr Design mit flexiblen Abschnittsoptionen!
type: docs
weight: 190
url: /de/net/aspose.words/pagesetup/layoutmode/
---
## PageSetup.LayoutMode property

Ruft den Layoutmodus dieses Abschnitts ab oder legt ihn fest.

```csharp
public SectionLayoutMode LayoutMode { get; set; }
```

## Beispiele

Zeigt, wie Sie für die Anzahl der Zeichen angeben, die jede Zeile enthalten darf.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Pitching aktivieren und dann damit die Anzahl der Zeichen pro Zeile in diesem Abschnitt festlegen.
builder.PageSetup.LayoutMode = SectionLayoutMode.Grid;
builder.PageSetup.CharactersPerLine = 10;

// Die Anzahl der Zeichen hängt auch von der Schriftgröße ab.
doc.Styles["Normal"].Font.Size = 20;

Assert.AreEqual(8, doc.FirstSection.PageSetup.CharactersPerLine);

builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.Save(ArtifactsDir + "PageSetup.CharactersPerLine.docx");
```

Zeigt, wie Sie eine Begrenzung für die Zeilenanzahl festlegen, die jede Seite haben darf.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Pitching aktivieren und dann damit die Zeilenanzahl pro Seite in diesem Abschnitt festlegen.
// Eine ausreichend große Schriftgröße verschiebt einige Zeilen auf die nächste Seite, um überlappende Zeichen zu vermeiden.
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
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
