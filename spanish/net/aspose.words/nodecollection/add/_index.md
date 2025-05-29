---
title: NodeCollection.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words para .NET
description: Descubra el método Add de NodeCollection para agregar nodos a su colección sin esfuerzo, mejorando la gestión de sus datos con facilidad y eficiencia.
type: docs
weight: 30
url: /es/net/aspose.words/nodecollection/add/
---
## NodeCollection.Add method

Agrega un nodo al final de la colección.

```csharp
public void Add(Node node)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| node | Node | El nodo que se agregará al final de la colección. |

### Excepciones

| excepción | condición |
| --- | --- |
| NotSupportedException | El[`NodeCollection`](../) es una colección "profunda". |

## Observaciones

El nodo se inserta como un elemento secundario en el objeto de nodo desde el cual se creó la colección.

Si el nodo que se está insertando se creó a partir de otro documento, debe utilizar [`ImportNode`](../../documentbase/importnode/) para importar el nodo al documento actual. Luego, el nodo importado se puede insertar en el documento actual.

## Ejemplos

Muestra cómo preparar un nuevo nodo de sección para su edición.

```csharp
Document doc = new Document();

// Un documento en blanco viene con una sección, que tiene un cuerpo, que a su vez tiene un párrafo.
//Podemos agregar contenidos a este documento añadiendo elementos como líneas de texto, formas o tablas a ese párrafo.
Assert.AreEqual(NodeType.Section, doc.GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Body, doc.Sections[0].GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Paragraph, doc.Sections[0].Body.GetChild(NodeType.Any, 0, true).NodeType);

// Si agregamos una nueva sección como esta, no tendrá cuerpo ni ningún otro nodo secundario.
doc.Sections.Add(new Section(doc));

Assert.AreEqual(0, doc.Sections[1].GetChildNodes(NodeType.Any, true).Count);

// Ejecute el método "EnsureMinimum" para agregar un cuerpo y un párrafo a esta sección para comenzar a editarla.
doc.LastSection.EnsureMinimum();

Assert.AreEqual(NodeType.Body, doc.Sections[1].GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Paragraph, doc.Sections[1].Body.GetChild(NodeType.Any, 0, true).NodeType);

doc.Sections[0].Body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Ver también

* class [Node](../../node/)
* class [NodeCollection](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
