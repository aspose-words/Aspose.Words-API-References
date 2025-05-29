---
title: ITextShaper.ShapeText
linktitle: ShapeText
articleTitle: ShapeText
second_title: Aspose.Words para .NET
description: Descubra el método ShapeText de iTextShaper, que genera de manera eficiente objetos Cluster a partir de fragmentos de texto, garantizando una alineación y un formato de texto precisos.
type: docs
weight: 10
url: /es/net/aspose.words.shaping/itextshaper/shapetext/
---
## ITextShaper.ShapeText method

Devuelve[`Cluster`](../../cluster/)objetos generados a partir de una secuencia de fragmentos de texto. La longitud de la matriz devuelta es igual a la longitud de*runs* . Si la ejecución en un índice tiene clústeres correspondientes, entonces el resultado en el mismo índice los tendrá registrados.

```csharp
public Cluster[][] ShapeText(string[] runs, Direction direction, UnicodeScript script, 
    FontFeature[] enabledFontFeatures, VariationAxisCoordinate[] variations)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| runs | String[] | Una secuencia de fragmentos de texto |
| direction | Direction | Una dirección de texto |
| script | UnicodeScript | Un guión |
| enabledFontFeatures | FontFeature[] | Un conjunto de funciones OpenType habilitadas explícitamente a tener en cuenta |
| variations | VariationAxisCoordinate[] | Valores del eje de variación de la fuente |

### Ver también

* class [Cluster](../../cluster/)
* enum [Direction](../../direction/)
* enum [UnicodeScript](../../unicodescript/)
* enum [FontFeature](../../fontfeature/)
* class [VariationAxisCoordinate](../../variationaxiscoordinate/)
* interface [ITextShaper](../)
* espacio de nombres [Aspose.Words.Shaping](../../../aspose.words.shaping/)
* asamblea [Aspose.Words](../../../)
