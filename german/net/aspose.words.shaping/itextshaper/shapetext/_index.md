---
title: ITextShaper.ShapeText
linktitle: ShapeText
articleTitle: ShapeText
second_title: Aspose.Words für .NET
description: Entdecken Sie die ShapeText-Methode von iTextShaper, die effizient Cluster-Objekte aus Textfragmenten generiert und so eine präzise Textformatierung und -ausrichtung gewährleistet.
type: docs
weight: 10
url: /de/net/aspose.words.shaping/itextshaper/shapetext/
---
## ITextShaper.ShapeText method

Rückgaben[`Cluster`](../../cluster/)Objekte, die aus einer Folge von Textfragmenten generiert werden. Die Länge des zurückgegebenen Arrays entspricht der Länge von*runs* . Wenn ein Lauf an einem Index entsprechende Cluster hat, werden diese im Ergebnis am gleichen Index aufgezeichnet.

```csharp
public Cluster[][] ShapeText(string[] runs, Direction direction, UnicodeScript script, 
    FontFeature[] enabledFontFeatures, VariationAxisCoordinate[] variations)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| runs | String[] | Eine Folge von Textfragmenten |
| direction | Direction | Eine Textrichtung |
| script | UnicodeScript | Ein Skript |
| enabledFontFeatures | FontFeature[] | Eine Reihe explizit aktivierter OpenType-Funktionen, die berücksichtigt werden sollten |
| variations | VariationAxisCoordinate[] | Werte der Variationsachse der Schriftart |

### Siehe auch

* class [Cluster](../../cluster/)
* enum [Direction](../../direction/)
* enum [UnicodeScript](../../unicodescript/)
* enum [FontFeature](../../fontfeature/)
* class [VariationAxisCoordinate](../../variationaxiscoordinate/)
* interface [ITextShaper](../)
* namensraum [Aspose.Words.Shaping](../../../aspose.words.shaping/)
* Montage [Aspose.Words](../../../)
