---
title: BorderCollection.Color
linktitle: Color
articleTitle: Color
second_title: Aspose.Words für .NET
description: Entdecken Sie die BorderCollection-Farbeigenschaft, um Rahmenfarben für Ihre Designs einfach anzupassen und zu verwalten. Verbessern Sie Ihre Benutzeroberfläche mit lebendigen Optionen!
type: docs
weight: 20
url: /de/net/aspose.words/bordercollection/color/
---
## BorderCollection.Color property

Ruft die Rahmenfarbe ab oder legt sie fest.

```csharp
public Color Color { get; set; }
```

## Bemerkungen

Gibt die Farbe des ersten Rahmens in der Sammlung zurück.

Legt die Farbe aller Rahmen in der Sammlung fest, mit Ausnahme diagonaler Rahmen.

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
