---
title: DocumentBuilder.MoveToDocumentStart
second_title: Referencia de API de Aspose.Words para .NET
description: DocumentBuilder método. Mueve el cursor al principio del documento.
type: docs
weight: 500
url: /es/net/aspose.words/documentbuilder/movetodocumentstart/
---
## DocumentBuilder.MoveToDocumentStart method

Mueve el cursor al principio del documento.

```csharp
public void MoveToDocumentStart()
```

### Ejemplos

Muestra cómo mover el cursor de un generador de documentos a diferentes nodos en un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Crear un marcador válido, una entidad que consta de nodos encerrados por un nodo de inicio de marcador,
  // y un nodo final de marcador.
builder.StartBookmark("MyBookmark");
builder.Write("Bookmark contents.");
builder.EndBookmark("MyBookmark");

NodeCollection firstParagraphNodes = doc.FirstSection.Body.FirstParagraph.ChildNodes;

Assert.AreEqual(NodeType.BookmarkStart, firstParagraphNodes[0].NodeType);
Assert.AreEqual(NodeType.Run, firstParagraphNodes[1].NodeType);
Assert.AreEqual("Bookmark contents.", firstParagraphNodes[1].GetText().Trim());
Assert.AreEqual(NodeType.BookmarkEnd, firstParagraphNodes[2].NodeType);

// El cursor del generador de documentos siempre está delante del último nodo que agregamos con él.
// Si el cursor del constructor está al final del documento, su nodo actual será nulo.
// El nodo anterior es el nodo final del marcador que agregamos por última vez.
// Agregar nuevos nodos con el constructor los agregará al último nodo.
Assert.Null(builder.CurrentNode);

// Si deseamos editar una parte diferente del documento con el constructor,
// necesitaremos llevar su cursor al nodo que deseamos editar.
builder.MoveToBookmark("MyBookmark");

// Moverlo a un marcador lo moverá al primer nodo dentro de los nodos de inicio y final del marcador, la ejecución adjunta.
Assert.AreEqual(firstParagraphNodes[1], builder.CurrentNode);

// También podemos mover el cursor a un nodo individual como este.
builder.MoveTo(doc.FirstSection.Body.FirstParagraph.GetChildNodes(NodeType.Any, false)[0]);

Assert.AreEqual(NodeType.BookmarkStart, builder.CurrentNode.NodeType);
Assert.AreEqual(doc.FirstSection.Body.FirstParagraph, builder.CurrentParagraph);
Assert.IsTrue(builder.IsAtStartOfParagraph);

// Podemos usar métodos específicos para movernos al inicio/final de un documento.
builder.MoveToDocumentEnd();

Assert.IsTrue(builder.IsAtEndOfParagraph);

builder.MoveToDocumentStart();

Assert.IsTrue(builder.IsAtStartOfParagraph);
```

### Ver también

* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../documentbuilder/)
* asamblea [Aspose.Words](../../../)


