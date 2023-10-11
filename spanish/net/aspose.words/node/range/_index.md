---
title: Node.Range
second_title: Referencia de API de Aspose.Words para .NET
description: Node propiedad. Devuelve unRange objeto que representa la parte de un documento contenido en este nodo.
type: docs
weight: 80
url: /es/net/aspose.words/node/range/
---
## Node.Range property

Devuelve un[`Range`](../../range/) objeto que representa la parte de un documento contenido en este nodo.

```csharp
public Range Range { get; }
```

### Ejemplos

Muestra cómo eliminar todos los nodos de un rango.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Agrega texto a la primera sección del documento y luego agrega otra sección.
builder.Write("Section 1. ");
builder.InsertBreak(BreakType.SectionBreakContinuous);
builder.Write("Section 2.");

Assert.AreEqual("Section 1. \fSection 2.", doc.GetText().Trim());

// Elimina la primera sección por completo eliminando todos los nodos
// dentro de su rango, incluida la sección misma.
doc.Sections[0].Range.Delete();

Assert.AreEqual(1, doc.Sections.Count);
Assert.AreEqual("Section 2.", doc.GetText().Trim());
```

### Ver también

* class [Range](../../range/)
* class [Node](../)
* espacio de nombres [Aspose.Words](../../node/)
* asamblea [Aspose.Words](../../../)


