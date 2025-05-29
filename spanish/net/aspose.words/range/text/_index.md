---
title: Range.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words para .NET
description: Descubra la propiedad Texto de rango para recuperar y manipular fácilmente texto dentro de un rango específico para una mejor gestión de contenido.
type: docs
weight: 60
url: /es/net/aspose.words/range/text/
---
## Range.Text property

Obtiene el texto del rango.

```csharp
public string Text { get; }
```

## Observaciones

La cadena devuelta incluye todos los caracteres de control y especiales como se describe en[`ControlChar`](../../controlchar/).

## Ejemplos

Muestra cómo obtener el contenido de texto de todos los nodos que cubre un rango.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

Assert.AreEqual("Hello world!", doc.Range.Text.Trim());
```

### Ver también

* class [Range](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
