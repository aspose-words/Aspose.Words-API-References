---
title: BorderCollection.DistanceFromText
linktitle: DistanceFromText
articleTitle: DistanceFromText
second_title: Aspose.Words für .NET
description: Entdecken Sie die BorderCollection DistanceFromText-Eigenschaft, um den Rahmenabstand von Text in Ihren Designs einfach anzupassen. Optimieren Sie Ihr Layout mühelos!
type: docs
weight: 40
url: /de/net/aspose.words/bordercollection/distancefromtext/
---
## BorderCollection.DistanceFromText property

Ruft den Abstand des Rahmens vom Text in Punkten ab oder legt ihn fest.

```csharp
public double DistanceFromText { get; set; }
```

## Bemerkungen

Ruft den Abstand vom Text für den ersten Rahmen ab.

Legt den Abstand vom Text für alle Rahmen in der Sammlung fest, mit Ausnahme diagonaler Rahmen.

Hat keine Auswirkung und wird für die Ränder von Tabellenzellen automatisch auf Null zurückgesetzt.

## Beispiele

Zeigt, wie man einen grünen, gewellten Seitenrand mit Schatten erstellt.

```csharp
Document doc = new Document();
PageSetup pageSetup = doc.Sections[0].PageSetup;

pageSetup.Borders.LineStyle = LineStyle.DoubleWave;
pageSetup.Borders.LineWidth = 2;
pageSetup.Borders.Color = Color.Green;
pageSetup.Borders.DistanceFromText = 24;
pageSetup.Borders.Shadow = true;

doc.Save(ArtifactsDir + "PageSetup.PageBorders.docx");
```

### Siehe auch

* class [BorderCollection](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
