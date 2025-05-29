---
title: CompositeNode.RemoveChild
linktitle: RemoveChild
articleTitle: RemoveChild
second_title: Aspose.Words para .NET
description: Administre sin esfuerzo su CompositeNode con el método RemoveChild, diseñado para agilizar la eliminación de nodos para un mejor rendimiento y eficiencia.
type: docs
weight: 190
url: /es/net/aspose.words/compositenode/removechild/
---
## CompositeNode.RemoveChild&lt;T&gt; method

Elimina el nodo secundario especificado.

```csharp
public T RemoveChild<T>(T oldChild)
    where T : Node
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| oldChild | T | El nodo a eliminar. |

### Valor_devuelto

El nodo eliminado.

## Observaciones

El padre de*oldChild* está configurado para`nulo` después de eliminar el nodo.

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
