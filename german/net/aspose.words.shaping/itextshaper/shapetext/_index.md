---
title: ITextShaper.ShapeText
second_title: Aspose.Words für .NET-API-Referenz
description: ITextShaper methode. Gibt zurückClusterObjekte die aus einer Folge von Textfragmenten generiert werden. Die Länge des zurückgegebenen Arrays ist gleich der Länge vonruns . Wenn die Ausführung mit einem Index entsprechende Cluster aufweist werden diese beim Ergebnis mit demselben Index aufgezeichnet.
type: docs
weight: 10
url: /de/net/aspose.words.shaping/itextshaper/shapetext/
---
## ITextShaper.ShapeText method

Gibt zurück[`Cluster`](../../cluster/)Objekte, die aus einer Folge von Textfragmenten generiert werden. Die Länge des zurückgegebenen Arrays ist gleich der Länge von*runs* . Wenn die Ausführung mit einem Index entsprechende Cluster aufweist, werden diese beim Ergebnis mit demselben Index aufgezeichnet.

```csharp
public Cluster[][] ShapeText(string[] runs, Direction direction, UnicodeScript script, 
    params FontFeature[] fontFeatures)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| runs | String[] | Eine Folge von Textfragmenten |
| direction | Direction | Eine Textrichtung |
| script | UnicodeScript | Ein Skript |
| fontFeatures | FontFeature[] | Eine Reihe von Funktionen, die es zu berücksichtigen gilt |

### Siehe auch

* class [Cluster](../../cluster/)
* enum [Direction](../../direction/)
* enum [UnicodeScript](../../unicodescript/)
* enum [FontFeature](../../fontfeature/)
* interface [ITextShaper](../)
* namensraum [Aspose.Words.Shaping](../../itextshaper/)
* Montage [Aspose.Words](../../../)


