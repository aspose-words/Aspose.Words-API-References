---
title: Node.Range
linktitle: Range
articleTitle: Range
second_title: Aspose.Words para .NET
description: Descubra la propiedad Rango de nodo, acceda sin esfuerzo a un objeto Rango que define el segmento de documento dentro de su nodo para una mejor gestión de contenido.
type: docs
weight: 80
url: /es/net/aspose.words/node/range/
---
## Node.Range property

Devuelve un[`Range`](../../range/)objeto que representa la porción de un documento que está contenida en este nodo.

```csharp
public Range Range { get; }
```

## Ejemplos

Muestra cómo eliminar todos los nodos de un rango.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Agregue texto a la primera sección del documento y luego agregue otra sección.
builder.Write("Section 1. ");
builder.InsertBreak(BreakType.SectionBreakContinuous);
builder.Write("Section 2.");

Assert.AreEqual("Section 1. \fSection 2.", doc.GetText().Trim());

//Elimine la primera sección por completo eliminando todos los nodos
// dentro de su rango, incluida la sección misma.
doc.Sections[0].Range.Delete();

Assert.AreEqual(1, doc.Sections.Count);
Assert.AreEqual("Section 2.", doc.GetText().Trim());
```

### Ver también

* class [Range](../../range/)
* class [Node](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
