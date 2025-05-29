---
title: ParagraphFormat.SnapToGrid
linktitle: SnapToGrid
articleTitle: SnapToGrid
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die ParagraphFormat SnapToGrid-Eigenschaft die Layoutpräzision verbessert, indem sie Ihre Absätze für ein elegantes Erscheinungsbild an den Rasterlinien des Dokuments ausrichtet.
type: docs
weight: 300
url: /de/net/aspose.words/paragraphformat/snaptogrid/
---
## ParagraphFormat.SnapToGrid property

Gibt an, ob der aktuelle Absatz beim Layouten des Inhalts im Absatz die Einstellungen für Dokumentrasterlinien pro Seite verwenden soll .

```csharp
public bool SnapToGrid { get; set; }
```

## Beispiele

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

* class [ParagraphFormat](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
