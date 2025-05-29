---
title: Border.Shadow
linktitle: Shadow
articleTitle: Shadow
second_title: Aspose.Words für .NET
description: Entdecken Sie die Border Shadow-Eigenschaft, um Ihr Design zu verbessern! Steuern Sie Schatteneffekte für Rahmen und werten Sie Ihre Benutzeroberfläche mit atemberaubenden Grafiken auf.
type: docs
weight: 60
url: /de/net/aspose.words/border/shadow/
---
## Border.Shadow property

Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob der Rahmen einen Schatten hat.

```csharp
public bool Shadow { get; set; }
```

## Bemerkungen

Damit ein Rahmen in Microsoft Word einen Schatten hat, müssen die Rahmen auf allen vier Seiten (links, oben, rechts und unten) vom gleichen Typ, der gleichen Breite und Farbe sein und alle müssen die Schatteneigenschaft auf`WAHR`.

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

* class [Border](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
