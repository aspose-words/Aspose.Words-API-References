---
title: Document.EnsureMinimum
linktitle: EnsureMinimum
articleTitle: EnsureMinimum
second_title: Aspose.Words para .NET
description: Aprenda a utilizar el método EnsureMinimum para crear automáticamente una sección y un párrafo en los documentos, garantizando un contenido completo y organizado.
type: docs
weight: 620
url: /es/net/aspose.words/document/ensureminimum/
---
## Document.EnsureMinimum method

Si el documento no contiene secciones, crea una sección con un párrafo.

```csharp
public void EnsureMinimum()
```

## Ejemplos

Muestra cómo garantizar que un documento contenga el conjunto mínimo de nodos necesarios para editar su contenido.

```csharp
// Un documento recién creado contiene una Sección secundaria, que incluye un Cuerpo secundario y un Párrafo secundario.
//Podemos editar el contenido del cuerpo del documento agregando nodos como Ejecuciones o Formas en línea a ese párrafo.
Document doc = new Document();
NodeCollection nodes = doc.GetChildNodes(NodeType.Any, true);

Assert.AreEqual(NodeType.Section, nodes[0].NodeType);
Assert.AreEqual(doc, nodes[0].ParentNode);

Assert.AreEqual(NodeType.Body, nodes[1].NodeType);
Assert.AreEqual(nodes[0], nodes[1].ParentNode);

Assert.AreEqual(NodeType.Paragraph, nodes[2].NodeType);
Assert.AreEqual(nodes[1], nodes[2].ParentNode);

// Este es el conjunto mínimo de nodos que necesitamos para poder editar el documento.
//Ya no podremos editar el documento si eliminamos alguno de ellos.
doc.RemoveAllChildren();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Any, true).Count);

//Llame a este método para asegurarse de que el documento tenga al menos esos tres nodos para que podamos editarlo nuevamente.
doc.EnsureMinimum();

Assert.AreEqual(NodeType.Section, nodes[0].NodeType);
Assert.AreEqual(NodeType.Body, nodes[1].NodeType);
Assert.AreEqual(NodeType.Paragraph, nodes[2].NodeType);

((Paragraph)nodes[2]).Runs.Add(new Run(doc, "Hello world!"));
```

### Ver también

* class [Document](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
