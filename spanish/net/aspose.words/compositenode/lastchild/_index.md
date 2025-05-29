---
title: CompositeNode.LastChild
linktitle: LastChild
articleTitle: LastChild
second_title: Aspose.Words para .NET
description: Descubra la propiedad CompositeNode LastChild para acceder y manipular fácilmente el último nodo hijo, mejorando la gestión de su estructura de datos.
type: docs
weight: 50
url: /es/net/aspose.words/compositenode/lastchild/
---
## CompositeNode.LastChild property

Obtiene el último hijo del nodo.

```csharp
public Node LastChild { get; }
```

## Observaciones

Si no hay un último nodo hijo, un`nulo` se devuelve.

## Ejemplos

Muestra cómo utilizar los métodos Node y CompositeNode para eliminar una sección antes de la última sección del documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Section 1 text.");
builder.InsertBreak(BreakType.SectionBreakContinuous);
builder.Writeln("Section 2 text.");

//Ambas secciones son hermanas entre sí.
Section lastSection = (Section)doc.LastChild;
Section firstSection = (Section)lastSection.PreviousSibling;

// Eliminar una sección en función de su relación con otra sección.
if (lastSection.PreviousSibling != null)
    doc.RemoveChild(firstSection);

//La sección que eliminamos fue la primera, dejando el documento solo con la segunda.
Assert.AreEqual("Section 2 text.", doc.GetText().Trim());
```

### Ver también

* class [Node](../../node/)
* class [CompositeNode](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
