---
title: Body.EnsureMinimum
linktitle: EnsureMinimum
articleTitle: EnsureMinimum
second_title: Aspose.Words para .NET
description: Body EnsureMinimum método. Si el último elemento secundario no es un párrafo crea y agrega un párrafo vacío en C#.
type: docs
weight: 50
url: /es/net/aspose.words/body/ensureminimum/
---
## Body.EnsureMinimum method

Si el último elemento secundario no es un párrafo, crea y agrega un párrafo vacío.

```csharp
public void EnsureMinimum()
```

## Ejemplos

Borra el texto principal de todas las secciones del documento, dejando las secciones mismas.

```csharp
Document doc = new Document();

// Un documento en blanco contiene una sección, un cuerpo y un párrafo.
// Llama al método "RemoveAllChildren" para eliminar todos esos nodos,
// y terminar con un nodo de documento sin hijos.
doc.RemoveAllChildren();

// Este documento ahora no tiene nodos secundarios compuestos a los que podamos agregar contenido.
// Si deseamos editarlo, necesitaremos volver a llenar su colección de nodos.
// Primero, crea una nueva sección y luego agrégala como secundaria al nodo del documento raíz.
Section section = new Section(doc);
doc.AppendChild(section);

// Una sección necesita un cuerpo, que contendrá y mostrará todo su contenido
// en la página entre el encabezado y el pie de página de la sección.
Body body = new Body(doc);
section.AppendChild(body);

// Este cuerpo no tiene hijos, por lo que todavía no podemos agregarle ejecuciones.
Assert.AreEqual(0, doc.FirstSection.Body.GetChildNodes(NodeType.Any, true).Count);

 // Llame a "EnsureMinimum" para asegurarse de que este cuerpo contenga al menos un párrafo vacío.
body.EnsureMinimum();

// Ahora podemos agregar ejecuciones al cuerpo y hacer que el documento las muestre.
body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Ver también

* class [Body](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
