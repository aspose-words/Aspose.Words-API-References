---
title: ITextShaper.ShapeText
second_title: Aspose.Words för .NET API Referens
description: ITextShaper metod. ReturnerarClusterobjekt genererade från en sekvens av textfragment. Längden på den returnerade arrayen är lika med längden påruns . Om körning på ett index har motsvarande kluster kommer resultatet på samma index att registreras.
type: docs
weight: 10
url: /sv/net/aspose.words.shaping/itextshaper/shapetext/
---
## ITextShaper.ShapeText method

Returnerar[`Cluster`](../../cluster/)objekt genererade från en sekvens av textfragment. Längden på den returnerade arrayen är lika med längden på*runs* . Om körning på ett index har motsvarande kluster kommer resultatet på samma index att registreras.

```csharp
public Cluster[][] ShapeText(string[] runs, Direction direction, UnicodeScript script, 
    params FontFeature[] fontFeatures)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| runs | String[] | En sekvens av textfragment |
| direction | Direction | En textriktning |
| script | UnicodeScript | Ett manus |
| fontFeatures | FontFeature[] | En uppsättning funktioner att överväga |

### Se även

* class [Cluster](../../cluster/)
* enum [Direction](../../direction/)
* enum [UnicodeScript](../../unicodescript/)
* enum [FontFeature](../../fontfeature/)
* interface [ITextShaper](../)
* namnutrymme [Aspose.Words.Shaping](../../itextshaper/)
* hopsättning [Aspose.Words](../../../)


