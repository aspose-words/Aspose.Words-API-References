---
title: DocumentBuilder.CurrentNode
linktitle: CurrentNode
articleTitle: CurrentNode
second_title: Aspose.Words para .NET
description: Descubra la propiedad CurrentNode de DocumentBuilder para acceder fácilmente al nodo seleccionado, mejorando la eficiencia y el flujo de trabajo de edición de documentos.
type: docs
weight: 40
url: /es/net/aspose.words/documentbuilder/currentnode/
---
## DocumentBuilder.CurrentNode property

Obtiene el nodo que está seleccionado actualmente en este DocumentBuilder.

```csharp
public Node CurrentNode { get; }
```

## Observaciones

`CurrentNode` es un cursor de[`DocumentBuilder`](../) y señala un[`Node`](../../node/) que es un hijo directo de un[`Paragraph`](../../paragraph/) Cualquier operación de inserción que realice utilizando [`DocumentBuilder`](../) se insertará antes del`CurrentNode`.

Cuando el párrafo actual está vacío o el cursor está posicionado justo antes del final de un párrafo o una etiqueta de documento estructurado,`CurrentNode` devoluciones`nulo`.

## Ejemplos

Muestra cómo mover el cursor de un generador de documentos a diferentes nodos en un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Crea un marcador válido, una entidad que consta de nodos encerrados por un nodo de inicio de marcador,
 // y un nodo final de marcador.
builder.StartBookmark("MyBookmark");
builder.Write("Bookmark contents.");
builder.EndBookmark("MyBookmark");

NodeCollection firstParagraphNodes = doc.FirstSection.Body.FirstParagraph.GetChildNodes(NodeType.Any, false);

Assert.AreEqual(NodeType.BookmarkStart, firstParagraphNodes[0].NodeType);
Assert.AreEqual(NodeType.Run, firstParagraphNodes[1].NodeType);
Assert.AreEqual("Bookmark contents.", firstParagraphNodes[1].GetText().Trim());
Assert.AreEqual(NodeType.BookmarkEnd, firstParagraphNodes[2].NodeType);

//El cursor del generador de documentos siempre está delante del último nodo que agregamos con él.
// Si el cursor del constructor está al final del documento, su nodo actual será nulo.
//El nodo anterior es el nodo final del marcador que agregamos por última vez.
// Agregar nuevos nodos con el constructor los agregará al último nodo.
Assert.Null(builder.CurrentNode);

// Si deseamos editar una parte diferente del documento con el constructor,
// necesitaremos llevar el cursor al nodo que deseamos editar.
builder.MoveToBookmark("MyBookmark");

// Moverlo a un marcador lo moverá al primer nodo dentro de los nodos de inicio y final del marcador, la ejecución adjunta.
Assert.AreEqual(firstParagraphNodes[1], builder.CurrentNode);

// También podemos mover el cursor a un nodo individual como este.
builder.MoveTo(doc.FirstSection.Body.FirstParagraph.GetChildNodes(NodeType.Any, false)[0]);

Assert.AreEqual(NodeType.BookmarkStart, builder.CurrentNode.NodeType);
Assert.AreEqual(doc.FirstSection.Body.FirstParagraph, builder.CurrentParagraph);
Assert.IsTrue(builder.IsAtStartOfParagraph);

//Podemos utilizar métodos específicos para movernos al inicio/final de un documento.
builder.MoveToDocumentEnd();

Assert.IsTrue(builder.IsAtEndOfParagraph);

builder.MoveToDocumentStart();

Assert.IsTrue(builder.IsAtStartOfParagraph);
```

### Ver también

* class [Node](../../node/)
* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
