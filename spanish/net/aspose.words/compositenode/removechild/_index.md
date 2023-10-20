---
title: CompositeNode.RemoveChild
linktitle: RemoveChild
articleTitle: RemoveChild
second_title: Aspose.Words para .NET
description: CompositeNode RemoveChild método. Elimina el nodo secundario especificado en C#.
type: docs
weight: 170
url: /es/net/aspose.words/compositenode/removechild/
---
## CompositeNode.RemoveChild method

Elimina el nodo secundario especificado.

```csharp
public Node RemoveChild(Node oldChild)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| oldChild | Node | El nodo que se va a eliminar. |

### Valor_devuelto

El nodo eliminado.

## Observaciones

el padre de*oldChild* se establece en`nulo` después de que se extrae el ganglio.

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

* class [Node](../../node/)
* class [CompositeNode](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
