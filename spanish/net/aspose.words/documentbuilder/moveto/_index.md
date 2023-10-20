---
title: DocumentBuilder.MoveTo
linktitle: MoveTo
articleTitle: MoveTo
second_title: Aspose.Words para .NET
description: DocumentBuilder MoveTo método. Mueve el cursor a un nodo en línea o al final de un párrafo en C#.
type: docs
weight: 480
url: /es/net/aspose.words/documentbuilder/moveto/
---
## DocumentBuilder.MoveTo method

Mueve el cursor a un nodo en línea o al final de un párrafo.

```csharp
public void MoveTo(Node node)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| node | Node | El nodo debe ser un párrafo o un hijo directo de un párrafo. |

## Observaciones

Cuandonodo es un nodo de nivel en línea, el cursor se mueve a este nodo y se insertará más contenido antes de ese nodo.

Cuandonodo es un[`Paragraph`](../../paragraph/), el cursor se mueve al final del párrafo y se insertará más contenido justo antes del salto de párrafo.

Cuandonodo es un nodo a nivel de bloque pero no un[`Paragraph`](../../paragraph/), el cursor se mueve al final del primer párrafo en el nivel de bloque node y se insertará más contenido justo antes del salto de párrafo.

## Ejemplos

Muestra cómo mover la posición del cursor de DocumentBuilder a un nodo específico.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Run 1. ");

// El generador de documentos tiene un cursor, que actúa como parte del documento
// donde el constructor agrega nuevos nodos cuando usamos sus métodos de construcción de documentos.
// Este cursor funciona de la misma manera que el cursor parpadeante de Microsoft Word,
// y también siempre termina inmediatamente después de cualquier nodo que el constructor acaba de insertar.
// Para agregar contenido a una parte diferente del documento,
// podemos mover el cursor a un nodo diferente con el método "MoveTo".
builder.MoveTo(doc.FirstSection.Body.FirstParagraph.Runs[0]);
// El cursor ahora está frente al nodo al que lo movimos.
// Agregar una segunda ejecución la insertará delante de la primera ejecución.
builder.Writeln("Run 2. ");

Assert.AreEqual("Run 2. \rRun 1.", doc.GetText().Trim());

// Mueva el cursor al final del documento para continuar agregando texto hasta el final como antes.
builder.MoveTo(doc.LastSection.Body.LastParagraph);
builder.Writeln("Run 3. ");

Assert.AreEqual("Run 2. \rRun 1. \rRun 3.", doc.GetText().Trim());
```

Muestra cómo mover el cursor de un generador de documentos a diferentes nodos de un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Crea un marcador válido, una entidad que consta de nodos encerrados por un nodo de inicio del marcador,
 // y un nodo final de marcador.
builder.StartBookmark("MyBookmark");
builder.Write("Bookmark contents.");
builder.EndBookmark("MyBookmark");

NodeCollection firstParagraphNodes = doc.FirstSection.Body.FirstParagraph.GetChildNodes(NodeType.Any, false);

Assert.AreEqual(NodeType.BookmarkStart, firstParagraphNodes[0].NodeType);
Assert.AreEqual(NodeType.Run, firstParagraphNodes[1].NodeType);
Assert.AreEqual("Bookmark contents.", firstParagraphNodes[1].GetText().Trim());
Assert.AreEqual(NodeType.BookmarkEnd, firstParagraphNodes[2].NodeType);

// El cursor del generador de documentos siempre está delante del nodo que agregamos por última vez.
// Si el cursor del constructor está al final del documento, su nodo actual será nulo.
// El nodo anterior es el nodo final del marcador que agregamos por última vez.
// Agregar nuevos nodos con el constructor los agregará al último nodo.
Assert.Null(builder.CurrentNode);

// Si deseamos editar una parte diferente del documento con el constructor,
// necesitaremos llevar el cursor al nodo que deseamos editar.
builder.MoveToBookmark("MyBookmark");

// Al moverlo a un marcador, se moverá al primer nodo dentro de los nodos de inicio y fin del marcador, la ejecución adjunta.
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

* class [Node](../../node/)
* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
