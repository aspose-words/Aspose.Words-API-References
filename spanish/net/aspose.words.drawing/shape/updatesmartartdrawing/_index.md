---
title: Shape.UpdateSmartArtDrawing
linktitle: UpdateSmartArtDrawing
articleTitle: UpdateSmartArtDrawing
second_title: Aspose.Words para .NET
description: Shape UpdateSmartArtDrawing método. Actualiza el dibujo prerenderizado de SmartArt utilizando el motor de renderizado en frío SmartArt de Aspose.Words en C#.
type: docs
weight: 250
url: /es/net/aspose.words.drawing/shape/updatesmartartdrawing/
---
## Shape.UpdateSmartArtDrawing method

Actualiza el dibujo prerenderizado de SmartArt utilizando el motor de renderizado en frío SmartArt de Aspose.Words.

```csharp
public void UpdateSmartArtDrawing()
```

## Observaciones

Microsoft Word genera y guarda el dibujo pre-renderizado junto con el objeto SmartArt. Sin embargo, si otras aplicaciones guardan el documento, es posible que el dibujo SmartArt pre-renderizado falte o sea incorrecto. Si el dibujo pre-renderizado está disponible, Aspose.Words lo usa para representar el objeto SmartArt. Si el dibujo pre-renderizado falta, entonces Aspose.Words usa su propio motor de renderizado en frío SmartArt para renderizar el objeto SmartArt. Si el dibujo prerenderizado es incorrecto, entonces es necesario llamar a este método para invocar el motor de renderizado SmartArt cold .

### Ver también

* class [Shape](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
