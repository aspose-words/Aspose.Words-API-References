---
title: ITextShaper.ShapeText
linktitle: ShapeText
articleTitle: ShapeText
second_title: Aspose.Words för .NET
description: Upptäck iTextShapers ShapeText-metod, som effektivt genererar klusterobjekt från textfragment, vilket säkerställer exakt textformatering och justering.
type: docs
weight: 10
url: /sv/net/aspose.words.shaping/itextshaper/shapetext/
---
## ITextShaper.ShapeText method

Returer[`Cluster`](../../cluster/)objekt genererade från en sekvens av textfragment. Längden på den returnerade arrayen är lika med längden på*runs* . Om körning vid ett index har motsvarande kluster, kommer resultatet vid samma index att få dem registrerade.

```csharp
public Cluster[][] ShapeText(string[] runs, Direction direction, UnicodeScript script, 
    FontFeature[] enabledFontFeatures, VariationAxisCoordinate[] variations)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| runs | String[] | En sekvens av textfragment |
| direction | Direction | En textriktning |
| script | UnicodeScript | Ett manus |
| enabledFontFeatures | FontFeature[] | En uppsättning explicit aktiverade OpenType-funktioner att beakta |
| variations | VariationAxisCoordinate[] | Typsnittets variationsaxelvärden |

### Se även

* class [Cluster](../../cluster/)
* enum [Direction](../../direction/)
* enum [UnicodeScript](../../unicodescript/)
* enum [FontFeature](../../fontfeature/)
* class [VariationAxisCoordinate](../../variationaxiscoordinate/)
* interface [ITextShaper](../)
* namnutrymme [Aspose.Words.Shaping](../../../aspose.words.shaping/)
* hopsättning [Aspose.Words](../../../)
