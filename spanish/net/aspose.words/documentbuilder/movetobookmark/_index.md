---
title: DocumentBuilder.MoveToBookmark
linktitle: MoveToBookmark
articleTitle: MoveToBookmark
second_title: Aspose.Words para .NET
description: Navegue sin esfuerzo por sus documentos con el método MoveToBookmark de DocumentBuilder, posicionando instantáneamente el cursor en cualquier marcador para una edición mejorada.
type: docs
weight: 530
url: /es/net/aspose.words/documentbuilder/movetobookmark/
---
## MoveToBookmark(*string*) {#movetobookmark}

Mueve el cursor a un marcador.

```csharp
public bool MoveToBookmark(string bookmarkName)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| bookmarkName | String | El nombre del marcador al que se moverá el cursor. |

### Valor_devuelto

`verdadero` si se encontró el marcador;`FALSO` de lo contrario.

## Observaciones

Mueve el cursor a una posición justo después del inicio del marcador con el nombre especificado .

La comparación no distingue entre mayúsculas y minúsculas. Si no se encontró el marcador,`FALSO` se devolvió is y el cursor no se movió.

Insertar texto nuevo no reemplaza el texto existente del marcador.

Tenga en cuenta que algunos marcadores del documento están asignados a campos de formulario. Al desplazarse a un marcador e insertar texto en él, este se inserta en el código del campo de formulario . Aunque esto no invalidará el campo de formulario, el texto insertado no será visible, ya que formará parte del código del campo.

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

* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

---

## MoveToBookmark(*string, bool, bool*) {#movetobookmark_1}

Mueve el cursor a un marcador con mayor precisión.

```csharp
public bool MoveToBookmark(string bookmarkName, bool isStart, bool isAfter)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| bookmarkName | String | El nombre del marcador al que se moverá el cursor. |
| isStart | Boolean | Cuando`verdadero` , mueve el cursor al principio del marcador. Cuando`FALSO`, mueve el cursor al final del marcador. |
| isAfter | Boolean | Cuando`verdadero` , mueve el cursor para ubicarlo después de la posición inicial o final del marcador . Cuando`FALSO`mueve el cursor para ubicarse antes de la posición inicial o final del marcador . |

### Valor_devuelto

`verdadero` si se encontró el marcador;`FALSO` de lo contrario.

## Observaciones

Mueve el cursor a una posición antes o después del inicio o el final del marcador.

Si la posición deseada no está a nivel de línea, pasa al siguiente párrafo.

La comparación no distingue entre mayúsculas y minúsculas. Si no se encontró el marcador,`FALSO` se devolvió is y el cursor no se movió.

## Ejemplos

Muestra cómo mover el cursor del punto de inserción del nodo de un generador de documentos a un marcador.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Un marcador válido consta de un nodo BookmarkStart, un nodo BookmarkEnd con un
// el nombre del marcador coincidente en algún lugar después, y el contenido encerrado por esos nodos.
builder.StartBookmark("MyBookmark");
builder.Write("Hello world! ");
builder.EndBookmark("MyBookmark");

// Hay 4 formas de mover el cursor de un generador de documentos a un marcador.
// Si estamos entre los nodos BookmarkStart y BookmarkEnd, el cursor estará dentro del marcador.
// Esto significa que cualquier texto agregado por el constructor se convertirá en parte del marcador.
// 1 - Fuera del marcador, delante del nodo BookmarkStart:
Assert.True(builder.MoveToBookmark("MyBookmark", true, false));
builder.Write("1. ");

Assert.AreEqual("Hello world! ", doc.Range.Bookmarks["MyBookmark"].Text);
Assert.AreEqual("1. Hello world!", doc.GetText().Trim());

// 2 - Dentro del marcador, justo después del nodo BookmarkStart:
Assert.True(builder.MoveToBookmark("MyBookmark", true, true));
builder.Write("2. ");

Assert.AreEqual("2. Hello world! ", doc.Range.Bookmarks["MyBookmark"].Text);
Assert.AreEqual("1. 2. Hello world!", doc.GetText().Trim());

// 2 - Dentro del marcador, justo en frente del nodo BookmarkEnd:
Assert.True(builder.MoveToBookmark("MyBookmark", false, false));
builder.Write("3. ");

Assert.AreEqual("2. Hello world! 3. ", doc.Range.Bookmarks["MyBookmark"].Text);
Assert.AreEqual("1. 2. Hello world! 3.", doc.GetText().Trim());

// 4 - Fuera del marcador, después del nodo BookmarkEnd:
Assert.True(builder.MoveToBookmark("MyBookmark", false, true));
builder.Write("4.");

Assert.AreEqual("2. Hello world! 3. ", doc.Range.Bookmarks["MyBookmark"].Text);
Assert.AreEqual("1. 2. Hello world! 3. 4.", doc.GetText().Trim());
```

### Ver también

* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
