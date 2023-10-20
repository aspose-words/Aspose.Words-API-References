---
title: ITextShaper.ShapeText
linktitle: ShapeText
articleTitle: ShapeText
second_title: Aspose.Words para .NET
description: ITextShaper ShapeText método. DevolucionesClusterobjetos generados a partir de una secuencia de fragmentos de texto. La longitud de la matriz devuelta es igual a la longitud deruns . Si la ejecución en un índice tiene grupos correspondientes el resultado en el mismo índice los registrará en C#.
type: docs
weight: 10
url: /es/net/aspose.words.shaping/itextshaper/shapetext/
---
## ITextShaper.ShapeText method

Devoluciones[`Cluster`](../../cluster/)objetos generados a partir de una secuencia de fragmentos de texto. La longitud de la matriz devuelta es igual a la longitud de*runs* . Si la ejecución en un índice tiene grupos correspondientes, el resultado en el mismo índice los registrará.

```csharp
public Cluster[][] ShapeText(string[] runs, Direction direction, UnicodeScript script, 
    params FontFeature[] fontFeatures)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| runs | String[] | Una secuencia de fragmentos de texto. |
| direction | Direction | Una dirección de texto |
| script | UnicodeScript | Un guión |
| fontFeatures | FontFeature[] | Un conjunto de características a considerar |

### Ver también

* class [Cluster](../../cluster/)
* enum [Direction](../../direction/)
* enum [UnicodeScript](../../unicodescript/)
* enum [FontFeature](../../fontfeature/)
* interface [ITextShaper](../)
* espacio de nombres [Aspose.Words.Shaping](../../../aspose.words.shaping/)
* asamblea [Aspose.Words](../../../)
