---
title: ParagraphFormat.SnapToGrid
second_title: Aspose.Words für .NET-API-Referenz
description: ParagraphFormat eigendom. Gibt an ob der aktuelle Absatz die Dokumentrasterlinien pro Seite verwenden soll. Settings  wenn der Inhalt im Absatz angeordnet wird.
type: docs
weight: 290
url: /de/net/aspose.words/paragraphformat/snaptogrid/
---
## ParagraphFormat.SnapToGrid property

Gibt an, ob der aktuelle Absatz die Dokumentrasterlinien pro Seite verwenden soll. Settings , wenn der Inhalt im Absatz angeordnet wird.

```csharp
public bool SnapToGrid { get; set; }
```

### Beispiele

Zeigt, wie Sie einen Grenzwert für die Anzahl der Zeilen festlegen, die jede Seite haben darf.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Pitching aktivieren und dann verwenden, um die Anzahl der Zeilen pro Seite in diesem Abschnitt festzulegen.
// Eine ausreichend große Schriftgröße verschiebt einige Zeilen nach unten auf die nächste Seite, um überlappende Zeichen zu vermeiden.
builder.PageSetup.LayoutMode = SectionLayoutMode.LineGrid;
builder.PageSetup.LinesPerPage = 15;

builder.ParagraphFormat.SnapToGrid = true;

for (int i = 0; i < 30; i++)
    builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");

doc.Save(ArtifactsDir + "PageSetup.LinesPerPage.docx");
```

### Siehe auch

* class [ParagraphFormat](../)
* namensraum [Aspose.Words](../../paragraphformat/)
* Montage [Aspose.Words](../../../)


