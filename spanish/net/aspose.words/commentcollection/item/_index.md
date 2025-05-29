---
title: CommentCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words para .NET
description: Acceda fácilmente a comentarios específicos con la propiedad Item de CommentCollection. Recupere comentarios por índice para una gestión de contenido optimizada.
type: docs
weight: 10
url: /es/net/aspose.words/commentcollection/item/
---
## CommentCollection indexer

Recupera una[`Comment`](../../comment/) en el índice dado.

```csharp
public Comment this[int index] { get; }
```

| Parámetro | Descripción |
| --- | --- |
| index | Un índice de la colección. |

## Observaciones

El índice está basado en cero.

Se permiten índices negativos e indican acceso desde la parte posterior de la colección. Por ejemplo, -1 significa el último elemento, -2 significa el penúltimo y así sucesivamente.

Si el índice es mayor o igual que el número de elementos de la lista, esto devuelve una referencia nula.

Si el índice es negativo y su valor absoluto es mayor que la cantidad de elementos de la lista, esto devuelve una referencia nula.

## Ejemplos

Muestra cómo eliminar respuestas a comentarios.

```csharp
Document doc = new Document();

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");

doc.FirstSection.Body.FirstParagraph.AppendChild(comment);

comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "New reply");
comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "Another reply");

Assert.AreEqual(2, comment.Replies.Count); 

// A continuación se muestran dos formas de eliminar respuestas de un comentario.
// 1 - Utilice el método "RemoveReply" para eliminar las respuestas de un comentario individualmente:
comment.RemoveReply(comment.Replies[0]);

Assert.AreEqual(1, comment.Replies.Count);

// 2 - Utilice el método "RemoveAllReplies" para eliminar todas las respuestas de un comentario a la vez:
comment.RemoveAllReplies();

Assert.AreEqual(0, comment.Replies.Count);
```

### Ver también

* class [Comment](../../comment/)
* class [CommentCollection](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
