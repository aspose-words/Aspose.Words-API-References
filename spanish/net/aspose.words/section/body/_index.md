---
title: Body
second_title: Referencia de API de Aspose.Words para .NET
description: Devuelve el Cuerpo nodo hijo de la sección.
type: docs
weight: 20
url: /es/net/aspose.words/section/body/
---
## Section.Body property

Devuelve el **Cuerpo** nodo hijo de la sección.

```csharp
public Body Body { get; }
```

### Observaciones

**Cuerpo** contiene el texto principal de la sección.

Devuelve nulo si la sección no tiene un **Cuerpo** nodo entre sus hijos.

### Ejemplos

Borra el texto principal de todas las secciones del documento dejando las secciones en sí.

```csharp
Document doc = new Document();

// Un documento en blanco contiene una sección, un cuerpo y un párrafo.
// Llame al método "RemoveAllChildren" para eliminar todos esos nodos,
// y terminar con un nodo de documento sin hijos.
doc.RemoveAllChildren();

// Este documento ahora no tiene nodos secundarios compuestos a los que podamos agregar contenido.
// Si deseamos editarlo, necesitaremos volver a llenar su colección de nodos.
// Primero, cree una nueva sección y luego agréguela como elemento secundario al nodo del documento raíz.
Section section = new Section(doc);
doc.AppendChild(section);

// Una sección necesita un cuerpo, que contendrá y mostrará todo su contenido
// en la página entre el encabezado y el pie de página de la sección.
Body body = new Body(doc);
section.AppendChild(body);

// Este cuerpo no tiene hijos, por lo que no podemos agregarle ejecuciones todavía.
Assert.AreEqual(0, doc.FirstSection.Body.GetChildNodes(NodeType.Any, true).Count);

// Llame a "EnsureMinimum" para asegurarse de que este cuerpo contenga al menos un párrafo vacío. 
body.EnsureMinimum();

// Ahora, podemos agregar ejecuciones al cuerpo y hacer que el documento las muestre.
body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Ver también

* class [Body](../../body)
* class [Section](../../section)
* espacio de nombres [Aspose.Words](../../section)
* asamblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->