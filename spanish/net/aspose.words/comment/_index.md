---
title: Comment
second_title: Referencia de API de Aspose.Words para .NET
description: Representa un contenedor para el texto de un comentario.
type: docs
weight: 220
url: /es/net/aspose.words/comment/
---
## Comment class

Representa un contenedor para el texto de un comentario.

```csharp
public sealed class Comment : InlineStory
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [Comment](comment#constructor)(DocumentBase) | Inicializa una nueva instancia del **Comentario** clase. |
| [Comment](comment#constructor_1)(DocumentBase, string, string, DateTime) | Inicializa una nueva instancia del **Comentario** clase. |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Ancestor](../../aspose.words/comment/ancestor) { get; } | Devuelve el objeto Comentario principal. Devuelve nulo para comentarios de nivel superior. |
| [Author](../../aspose.words/comment/author) { get; set; } | Devuelve o establece el nombre del autor de un comentario. |
| [ChildNodes](../../aspose.words/compositenode/childnodes) { get; } | Obtiene todos los nodos secundarios inmediatos de este nodo. |
| [Count](../../aspose.words/compositenode/count) { get; } | Obtiene el número de hijos inmediatos de este nodo. |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | Especifica el identificador de nodo personalizado. |
| [DateTime](../../aspose.words/comment/datetime) { get; set; } | Obtiene la fecha y hora en que se realizó el comentario. |
| virtual [Document](../../aspose.words/node/document) { get; } | Obtiene el documento al que pertenece este nodo. |
| [Done](../../aspose.words/comment/done) { get; set; } | Obtiene o establece un indicador que indica que el comentario se ha marcado como finalizado. |
| [FirstChild](../../aspose.words/compositenode/firstchild) { get; } | Obtiene el primer hijo del nodo. |
| [FirstParagraph](../../aspose.words/inlinestory/firstparagraph) { get; } | Obtiene el primer párrafo de la historia. |
| [Font](../../aspose.words/inlinestory/font) { get; } | Proporciona acceso al formato de fuente del carácter ancla de este objeto. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes) { get; } | Devuelve verdadero si este nodo tiene nodos secundarios. |
| [Id](../../aspose.words/comment/id) { get; } | Obtiene el identificador del comentario. |
| [Initial](../../aspose.words/comment/initial) { get; set; } | Devuelve o establece las iniciales del usuario asociado a un comentario concreto. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite) { get; } | Devuelve verdadero ya que este nodo puede tener nodos secundarios. |
| [IsDeleteRevision](../../aspose.words/inlinestory/isdeleterevision) { get; } | Devuelve verdadero si este objeto se eliminó en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [IsInsertRevision](../../aspose.words/inlinestory/isinsertrevision) { get; } | Devuelve verdadero si este objeto se insertó en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [IsMoveFromRevision](../../aspose.words/inlinestory/ismovefromrevision) { get; } | Devoluciones **verdadero** si este objeto se movió (eliminó) en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [IsMoveToRevision](../../aspose.words/inlinestory/ismovetorevision) { get; } | Devoluciones **verdadero** si este objeto se movió (insertó) en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [LastChild](../../aspose.words/compositenode/lastchild) { get; } | Obtiene el último hijo del nodo. |
| [LastParagraph](../../aspose.words/inlinestory/lastparagraph) { get; } | Obtiene el último párrafo de la historia. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | Obtiene el nodo que sigue inmediatamente a este nodo. |
| override [NodeType](../../aspose.words/comment/nodetype) { get; } | Devoluciones **Tipo de nodo.Comentario** . |
| [Paragraphs](../../aspose.words/inlinestory/paragraphs) { get; } | Obtiene una colección de párrafos que son hijos inmediatos de la historia. |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | Obtiene el padre inmediato de este nodo. |
| [ParentParagraph](../../aspose.words/inlinestory/parentparagraph) { get; } | Recupera el padre[`Paragraph`](../paragraph) de este nodo. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | Obtiene el nodo inmediatamente anterior a este nodo. |
| [Range](../../aspose.words/node/range) { get; } | Devuelve un **Rango** objeto que representa la parte de un documento que está contenido en este nodo. |
| [Replies](../../aspose.words/comment/replies) { get; } | Devuelve una colección de[`Comment`](../comment) objetos que son hijos inmediatos del comentario especificado. |
| override [StoryType](../../aspose.words/comment/storytype) { get; } | Devoluciones **StoryType.Comentarios** . |
| [Tables](../../aspose.words/inlinestory/tables) { get; } | Obtiene una colección de tablas que son elementos secundarios inmediatos de la historia. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| override [Accept](../../aspose.words/comment/accept)(DocumentVisitor) | Acepta un visitante. |
| [AddReply](../../aspose.words/comment/addreply)(string, string, DateTime, string) | Agrega una respuesta a este comentario. |
| [AppendChild](../../aspose.words/compositenode/appendchild)(Node) | Agrega el nodo especificado al final de la lista de nodos secundarios para este nodo. |
| [Clone](../../aspose.words/node/clone)(bool) | Crea un duplicado del nodo. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator)() | Reservado para uso del sistema. IXPathNavigable. |
| [EnsureMinimum](../../aspose.words/inlinestory/ensureminimum)() | Si el último elemento secundario no es un párrafo, crea y agrega un párrafo vacío. |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | Obtiene el primer ancestro del especificado[`NodeType`](../nodetype) . |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | Obtiene el primer ancestro del tipo de objeto especificado. |
| [GetChild](../../aspose.words/compositenode/getchild)(NodeType, int, bool) | Devuelve un enésimo nodo secundario que coincide con el tipo especificado. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes)(NodeType, bool) | Devuelve una colección activa de nodos secundarios que coinciden con el tipo especificado. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator)() | Proporciona soporte para la iteración de cada estilo sobre los nodos secundarios de este nodo. |
| override [GetText](../../aspose.words/compositenode/gettext)() | Obtiene el texto de este nodo y de todos sus hijos. |
| [IndexOf](../../aspose.words/compositenode/indexof)(Node) | Devuelve el índice del nodo secundario especificado en la matriz de nodos secundarios. |
| [InsertAfter](../../aspose.words/compositenode/insertafter)(Node, Node) | Inserta el nodo especificado inmediatamente después del nodo de referencia especificado. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore)(Node, Node) | Inserta el nodo especificado inmediatamente antes del nodo de referencia especificado. |
| [NextPreOrder](../../aspose.words/node/nextpreorder)(Node) | Obtiene el siguiente nodo de acuerdo con el algoritmo de recorrido del árbol de pedido previo. |
| [PrependChild](../../aspose.words/compositenode/prependchild)(Node) | Agrega el nodo especificado al principio de la lista de nodos secundarios para este nodo. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder)(Node) | Obtiene el nodo anterior de acuerdo con el algoritmo de recorrido del árbol de pedido previo. |
| [Remove](../../aspose.words/node/remove)() | Se elimina a sí mismo del padre. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren)() | Elimina todos los nodos secundarios del nodo actual. |
| [RemoveAllReplies](../../aspose.words/comment/removeallreplies)() | Elimina todas las respuestas a este comentario. |
| [RemoveChild](../../aspose.words/compositenode/removechild)(Node) | Elimina el nodo secundario especificado. |
| [RemoveReply](../../aspose.words/comment/removereply)(Comment) | Elimina la respuesta especificada a este comentario. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags)() | Elimina todo[`SmartTag`](../../aspose.words.markup/smarttag) nodos descendientes del nodo actual. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes)(string) | Selecciona una lista de nodos que coinciden con la expresión XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode)(string) | Selecciona el primer nodo que coincide con la expresión XPath. |
| [SetText](../../aspose.words/comment/settext)(string) | Este es un método conveniente que permite configurar fácilmente el texto del comentario. |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | Exporta el contenido del nodo a una cadena en el formato especificado. |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | Exporta el contenido del nodo a una cadena utilizando las opciones de guardado especificadas. |

### Observaciones

Un comentario es una anotación que está anclada a una región de texto oa una posición en el texto. Un comentario puede contener una cantidad arbitraria de contenido a nivel de bloque.

si un[`Comment`](../comment) el objeto ocurre por sí solo, el comentario está anclado a la posición del[`Comment`](../comment) objeto.

Para anclar un comentario a una región de texto se requieren tres objetos:[`Comment`](../comment) , [`CommentRangeStart`](../commentrangestart) y[`CommentRangeEnd`](../commentrangeend) Los tres objetos deben compartir el mismo [`Id`](./id) valor.

[`Comment`](../comment) es un nodo de nivel en línea y solo puede ser un elemento secundario de[`Paragraph`](../paragraph).

[`Comment`](../comment) puede contener[`Paragraph`](../paragraph) y[`Table`](../../aspose.words.tables/table) nodos secundarios.

### Ejemplos

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
// fuera del margen derecho de la página y con una línea punteada que lo conecta con su párrafo.
builder.CurrentParagraph.AppendChild(comment);

// Agregue una respuesta, que aparecerá debajo de su comentario principal.
comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "New reply");

// Los comentarios y las respuestas son ambos nodos de comentarios.
Assert.AreEqual(2, doc.GetChildNodes(NodeType.Comment, true).Count);

// Los comentarios que no responden a otros comentarios son de "nivel superior". No tienen comentarios de antepasados.
Assert.Null(comment.Ancestor);

// Las respuestas tienen un comentario de nivel superior antepasado.
Assert.AreEqual(comment, comment.Replies[0].Ancestor);

doc.Save(ArtifactsDir + "Comment.AddCommentWithReply.docx");
```

### Ver también

* class [InlineStory](../inlinestory)
* espacio de nombres [Aspose.Words](../../aspose.words)
* asamblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
