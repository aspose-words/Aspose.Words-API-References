---
title: Range.Text
second_title: Referencia de API de Aspose.Words para .NET
description: Range propiedad. Obtiene el texto del rango.
type: docs
weight: 50
url: /es/net/aspose.words/range/text/
---
## Range.Text property

Obtiene el texto del rango.

```csharp
public string Text { get; }
```

### Observaciones

La cadena devuelta incluye todos los caracteres especiales y de control como se describe en[`ControlChar`](../../controlchar/).

### Ejemplos

Muestra cómo obtener el contenido de texto de todos los nodos que cubre un rango.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

Assert.AreEqual("Hello world!", doc.Range.Text.Trim());
```

### Ver también

* class [Range](../)
* espacio de nombres [Aspose.Words](../../range/)
* asamblea [Aspose.Words](../../../)


