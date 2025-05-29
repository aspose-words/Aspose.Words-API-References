---
title: Node.PreviousSibling
linktitle: PreviousSibling
articleTitle: PreviousSibling
second_title: Aspose.Words para .NET
description: Descubra la propiedad Node PreviousSibling para acceder fácilmente al nodo que viene antes de su nodo actual, mejorando sus habilidades de manipulación del DOM.
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

Si no hay ningún nodo precedente, un`nulo` se devuelve.

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

* class [Node](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
