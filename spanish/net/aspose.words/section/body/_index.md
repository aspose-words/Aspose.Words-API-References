---
title: Section.Body
linktitle: Body
articleTitle: Body
second_title: Aspose.Words para .NET
description: Descubra la propiedad Cuerpo de la sección que recupera el nodo secundario Cuerpo, mejorando su desarrollo web con una gestión de contenido optimizada.
type: docs
weight: 20
url: /es/net/aspose.words/section/body/
---
## Section.Body property

Devuelve el[`Body`](../../body/) nodo hijo de la sección.

```csharp
public Body Body { get; }
```

## Observaciones

[`Body`](../../body/) Contiene el texto principal de la sección.

Devoluciones`nulo` Si la sección no tiene una[`Body`](../../body/) nodo entre sus hijos.

## Ejemplos

Borra el texto principal de todas las secciones del documento, dejando solo las secciones mismas.

```csharp
Document doc = new Document();

// Un documento en blanco contiene una sección, un cuerpo y un párrafo.
// Llama al método "RemoveAllChildren" para eliminar todos esos nodos,
// y terminar con un nodo de documento sin hijos.
doc.RemoveAllChildren();

//Este documento ahora no tiene nodos secundarios compuestos a los que podamos agregar contenido.
// Si deseamos editarlo, necesitaremos volver a llenar su colección de nodos.
// Primero, cree una nueva sección y luego añádala como un elemento secundario al nodo del documento raíz.
Section section = new Section(doc);
doc.AppendChild(section);

// Una sección necesita un cuerpo, que contendrá y mostrará todo su contenido.
// en la página entre el encabezado y el pie de página de la sección.
Body body = new Body(doc);
section.AppendChild(body);

//Este cuerpo no tiene hijos, por lo que aún no podemos agregarle ejecuciones.
Assert.AreEqual(0, doc.FirstSection.Body.GetChildNodes(NodeType.Any, true).Count);

 // Llame a "EnsureMinimum" para asegurarse de que este cuerpo contenga al menos un párrafo vacío.
body.EnsureMinimum();

// Ahora, podemos agregar ejecuciones al cuerpo y hacer que el documento las muestre.
body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Ver también

* class [Body](../../body/)
* class [Section](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
