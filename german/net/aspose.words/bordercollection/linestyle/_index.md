---
title: BorderCollection.LineStyle
linktitle: LineStyle
articleTitle: LineStyle
second_title: Aspose.Words für .NET
description: Entdecken Sie die LineStyle-Eigenschaft der BorderCollection, um Ihr Design mit flexiblen Rahmenstilen anzupassen. Verbessern Sie mühelos die visuelle Attraktivität Ihres Projekts!
type: docs
weight: 80
url: /de/net/aspose.words/bordercollection/linestyle/
---
## BorderCollection.LineStyle property

Ruft den Rahmenstil ab oder legt ihn fest.

```csharp
public LineStyle LineStyle { get; set; }
```

## Bemerkungen

Gibt den Stil des ersten Rahmens in der Sammlung zurück.

Legt den Stil aller Rahmen in der Sammlung fest, mit Ausnahme diagonaler Rahmen.

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

* enum [LineStyle](../../linestyle/)
* class [BorderCollection](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
