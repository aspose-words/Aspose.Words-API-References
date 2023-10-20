---
title: Node.PreviousSibling
linktitle: PreviousSibling
articleTitle: PreviousSibling
second_title: Aspose.Words para .NET
description: Node PreviousSibling propiedad. Obtiene el nodo inmediatamente anterior a este nodo en C#.
type: docs
weight: 70
url: /es/net/aspose.words/node/previoussibling/
---
## Node.PreviousSibling property

Obtiene el nodo inmediatamente anterior a este nodo.

```csharp
public Node PreviousSibling { get; }
```

## Observaciones

Si no hay ningún nodo anterior, se`nulo` se devuelve.

## Ejemplos

Muestra cómo utilizar los métodos de Node y CompositeNode para eliminar una sección antes de la última sección del documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Section 1 text.");
builder.InsertBreak(BreakType.SectionBreakContinuous);
builder.Writeln("Section 2 text.");

// Ambas secciones son hermanas entre sí.
Section lastSection = (Section)doc.LastChild;
Section firstSection = (Section)lastSection.PreviousSibling;

// Elimina una sección según su relación de hermana con otra sección.
if (lastSection.PreviousSibling != null)
    doc.RemoveChild(firstSection);

// La sección que eliminamos fue la primera, dejando el documento solo con la segunda.
Assert.AreEqual("Section 2 text.", doc.GetText().Trim());
```

### Ver también

* class [Node](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
