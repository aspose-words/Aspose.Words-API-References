---
title: Comment Class
linktitle: Comment
articleTitle: Comment
second_title: Aspose.Words para .NET
description: Descubre la clase Aspose.Words.Comment, tu herramienta esencial para gestionar el texto de los comentarios en los documentos. ¡Mejora tu flujo de trabajo con una integración perfecta!
type: docs
weight: 420
url: /es/net/aspose.words/comment/
---
## Comment class

Representa un contenedor para el texto de un comentario.

Para obtener más información, visite el[Trabajar con comentarios](https://docs.aspose.com/words/net/working-with-comments/) Artículo de documentación.

```csharp
public sealed class Comment : InlineStory
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [Comment](comment/#constructor)(*[DocumentBase](../documentbase/)*) | Inicializa una nueva instancia del`Comment` clase. |
| [Comment](comment/#constructor_1)(*[DocumentBase](../documentbase/), string, string, DateTime*) | Inicializa una nueva instancia del`Comment` clase. |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Ancestor](../../aspose.words/comment/ancestor/) { get; } | Devuelve el padre`Comment`objeto. Devuelve`nulo` para comentarios de alto nivel. |
| [Author](../../aspose.words/comment/author/) { get; set; } | Devuelve o establece el nombre del autor de un comentario. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Obtiene el número de hijos inmediatos de este nodo. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Especifica un identificador de nodo personalizado. |
| [DateTime](../../aspose.words/comment/datetime/) { get; set; } | Obtiene la fecha y hora en que se realizó el comentario. |
| [DateTimeUtc](../../aspose.words/comment/datetimeutc/) { get; } | Obtiene la fecha y hora UTC en que se realizó el comentario. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Obtiene el documento al que pertenece este nodo. |
| [Done](../../aspose.words/comment/done/) { get; set; } | Obtiene o establece el indicador que indica que el comentario se ha marcado como hecho. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Obtiene el primer hijo del nodo. |
| [FirstParagraph](../../aspose.words/inlinestory/firstparagraph/) { get; } | Obtiene el primer párrafo de la historia. |
| [Font](../../aspose.words/inlinestory/font/) { get; } | Proporciona acceso al formato de fuente del carácter de anclaje de este objeto. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Devuelve`verdadero` si este nodo tiene nodos secundarios. |
| [Id](../../aspose.words/comment/id/) { get; set; } | Obtiene o establece el identificador del comentario. |
| [Initial](../../aspose.words/comment/initial/) { get; set; } | Devuelve o establece las iniciales del usuario asociado con un comentario específico. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Devuelve`verdadero` ya que este nodo puede tener nodos secundarios. |
| [IsDeleteRevision](../../aspose.words/inlinestory/isdeleterevision/) { get; } | Devuelve verdadero si este objeto se eliminó en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [IsInsertRevision](../../aspose.words/inlinestory/isinsertrevision/) { get; } | Devuelve verdadero si este objeto se insertó en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [IsMoveFromRevision](../../aspose.words/inlinestory/ismovefromrevision/) { get; } | Devuelve`verdadero` Si este objeto se movió (eliminó) en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [IsMoveToRevision](../../aspose.words/inlinestory/ismovetorevision/) { get; } | Devuelve`verdadero` Si este objeto se movió (insertó) en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Obtiene el último hijo del nodo. |
| [LastParagraph](../../aspose.words/inlinestory/lastparagraph/) { get; } | Obtiene el último párrafo de la historia. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Obtiene el nodo inmediatamente siguiente a este nodo. |
| override [NodeType](../../aspose.words/comment/nodetype/) { get; } | DevuelveComment . |
| [Paragraphs](../../aspose.words/inlinestory/paragraphs/) { get; } | Obtiene una colección de párrafos que son hijos inmediatos de la historia. |
| [ParentId](../../aspose.words/comment/parentid/) { get; set; } | Obtiene o establece el ID del comentario principal. Un valor de`-1` significa que el comentario no tiene padre. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Obtiene el padre inmediato de este nodo. |
| [ParentParagraph](../../aspose.words/inlinestory/parentparagraph/) { get; } | Recupera el padre[`Paragraph`](../paragraph/) de este nodo. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Obtiene el nodo inmediatamente anterior a este nodo. |
| [Range](../../aspose.words/node/range/) { get; } | Devuelve un[`Range`](../range/)objeto que representa la porción de un documento que está contenida en este nodo. |
| [Replies](../../aspose.words/comment/replies/) { get; } | Devuelve una colección de`Comment` objetos que son hijos inmediatos del comentario especificado. |
| override [StoryType](../../aspose.words/comment/storytype/) { get; } | DevuelveComments . |
| [Tables](../../aspose.words/inlinestory/tables/) { get; } | Obtiene una colección de tablas que son hijas inmediatas de la historia. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| override [Accept](../../aspose.words/comment/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Acepta un visitante. |
| override [AcceptEnd](../../aspose.words/comment/acceptend/)(*[DocumentVisitor](../documentvisitor/)*) | Acepta un visitante por visitar el final del comentario. |
| override [AcceptStart](../../aspose.words/comment/acceptstart/)(*[DocumentVisitor](../documentvisitor/)*) | Acepta un visitante por visitar el inicio del comentario. |
| [AddReply](../../aspose.words/comment/addreply/)(*string, string, DateTime, string*) | Agrega una respuesta a este comentario. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | Agrega el nodo especificado al final de la lista de nodos secundarios para este nodo. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Crea un duplicado del nodo. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Crea un navegador que puede utilizarse para recorrer y leer nodos. |
| [EnsureMinimum](../../aspose.words/inlinestory/ensureminimum/)() | Si el último hijo no es un párrafo, crea y agrega un párrafo vacío. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | Obtiene el primer ancestro del especificado[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Obtiene el primer ancestro del tipo de objeto especificado. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../nodetype/), int, bool*) | Devuelve un nodo secundario N que coincide con el tipo especificado. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../nodetype/), bool*) | Devuelve una colección activa de nodos secundarios que coinciden con el tipo especificado. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Proporciona soporte para cada iteración de estilo sobre los nodos secundarios de este nodo. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Obtiene el texto de este nodo y de todos sus hijos. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../node/)*) | Devuelve el índice del nodo secundario especificado en la matriz de nodos secundarios. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(*T, [Node](../node/)*) | Inserta el nodo especificado inmediatamente después del nodo de referencia especificado. |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(*T, [Node](../node/)*) | Inserta el nodo especificado inmediatamente antes del nodo de referencia especificado. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../node/)*) | Obtiene el siguiente nodo según el algoritmo de recorrido del árbol de preorden. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(*T*) | Agrega el nodo especificado al comienzo de la lista de nodos secundarios para este nodo. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../node/)*) | Obtiene el nodo anterior según el algoritmo de recorrido del árbol de preorden. |
| [Remove](../../aspose.words/node/remove/)() | Se elimina a sí mismo del padre. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Elimina todos los nodos secundarios del nodo actual. |
| [RemoveAllReplies](../../aspose.words/comment/removeallreplies/)() | Elimina todas las respuestas a este comentario. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(*T*) | Elimina el nodo secundario especificado. |
| [RemoveReply](../../aspose.words/comment/removereply/)(*Comment*) | Elimina la respuesta especificada a este comentario. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Elimina todo[`SmartTag`](../../aspose.words.markup/smarttag/) nodos descendientes del nodo actual. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | Selecciona una lista de nodos que coinciden con la expresión XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | Selecciona el primer[`Node`](../node/) que coincide con la expresión XPath. |
| [SetText](../../aspose.words/comment/settext/)(*string*) | Este es un método conveniente que permite configurar fácilmente el texto del comentario. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../saveformat/)*) | Exporta el contenido del nodo en una cadena en el formato especificado. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Exporta el contenido del nodo en una cadena utilizando las opciones de guardado especificadas. |

## Observaciones

Un comentario es una anotación que está anclada a una región de texto o a una posición en el texto. Un comentario puede contener una cantidad arbitraria de contenido a nivel de bloque.

Si un`Comment` El objeto aparece por sí solo, el comentario está anclado a la posición del`Comment` objeto.

Para anclar un comentario a una región de texto se requieren tres objetos:`Comment` , [`CommentRangeStart`](../commentrangestart/) y[`CommentRangeEnd`](../commentrangeend/) Los tres objetos deben compartir el mismo [`Id`](./id/) valor.

`Comment` es un nodo de nivel en línea y solo puede ser un hijo de[`Paragraph`](../paragraph/).

`Comment` puede contener[`Paragraph`](../paragraph/) y[`Table`](../../aspose.words.tables/table/) nodos secundarios.

## Ejemplos

Muestra cómo agregar un comentario a un párrafo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world!");

Comment comment = new Comment(doc, "John Doe", "JD", DateTime.Today);
builder.CurrentParagraph.AppendChild(comment);
builder.MoveTo(comment.AppendChild(new Paragraph(doc)));
builder.Write("Comment text.");

Assert.AreEqual(DateTime.Today, comment.DateTime);

 // En Microsoft Word, podemos hacer clic derecho en este comentario en el cuerpo del documento para editarlo o responderlo.
doc.Save(ArtifactsDir + "InlineStory.AddComment.docx");
```

Muestra cómo agregar un comentario a un documento y luego responderlo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");

// Coloque el comentario en un nodo en el cuerpo del documento.
// Este comentario se mostrará en la ubicación de su párrafo,
// fuera del margen derecho de la página, y con una línea punteada que lo conecta a su párrafo.
builder.CurrentParagraph.AppendChild(comment);

// Agregue una respuesta, que aparecerá debajo del comentario principal.
comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "New reply");

// Tanto los comentarios como las respuestas son nodos de comentarios.
Assert.AreEqual(2, doc.GetChildNodes(NodeType.Comment, true).Count);

Los comentarios que no responden a otros comentarios son de "nivel superior". No tienen comentarios antecesores.
Assert.Null(comment.Ancestor);

// Las respuestas tienen un comentario de nivel superior anterior.
Assert.AreEqual(comment, comment.Replies[0].Ancestor);

doc.Save(ArtifactsDir + "Comment.AddCommentWithReply.docx");
```

### Ver también

* class [InlineStory](../inlinestory/)
* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
