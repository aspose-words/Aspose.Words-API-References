---
title: CompositeNode.LastChild
second_title: Referencia de API de Aspose.Words para .NET
description: CompositeNode propiedad. Obtiene el último hijo del nodo.
type: docs
weight: 60
url: /es/net/aspose.words/compositenode/lastchild/
---
## CompositeNode.LastChild property

Obtiene el último hijo del nodo.

```csharp
public Node LastChild { get; }
```

### Observaciones

Si no hay un último nodo secundario, se devuelve un valor nulo.

### Ejemplos

Muestra cómo usar los métodos Node y CompositeNode para eliminar una sección antes de la última sección del documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Section 1 text.");
builder.InsertBreak(BreakType.SectionBreakContinuous);
builder.Writeln("Section 2 text.");

// Ambas secciones son hermanas entre sí.
Section lastSection = (Section)doc.LastChild;
Section firstSection = (Section)lastSection.PreviousSibling;

// Eliminar una sección en función de su relación de hermanos con otra sección.
if (lastSection.PreviousSibling != null)
    doc.RemoveChild(firstSection);

// La sección que eliminamos fue la primera, dejando el documento solo con la segunda.
Assert.AreEqual("Section 2 text.", doc.GetText().Trim());
```

### Ver también

* class [Node](../../node/)
* class [CompositeNode](../)
* espacio de nombres [Aspose.Words](../../compositenode/)
* asamblea [Aspose.Words](../../../)


