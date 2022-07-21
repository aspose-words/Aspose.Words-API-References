---
title: InlineStory
second_title: Referencia de API de Aspose.Words para .NET
description: Clase base para nodos de nivel en línea que pueden contener párrafos y tablas.
type: docs
weight: 3070
url: /es/net/aspose.words/inlinestory/
---
## InlineStory class

Clase base para nodos de nivel en línea que pueden contener párrafos y tablas.

```csharp
public abstract class InlineStory : CompositeNode
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [ChildNodes](../../aspose.words/compositenode/childnodes) { get; } | Obtiene todos los nodos secundarios inmediatos de este nodo. |
| [Count](../../aspose.words/compositenode/count) { get; } | Obtiene el número de hijos inmediatos de este nodo. |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | Especifica el identificador de nodo personalizado. |
| virtual [Document](../../aspose.words/node/document) { get; } | Obtiene el documento al que pertenece este nodo. |
| [FirstChild](../../aspose.words/compositenode/firstchild) { get; } | Obtiene el primer hijo del nodo. |
| [FirstParagraph](../../aspose.words/inlinestory/firstparagraph) { get; } | Obtiene el primer párrafo de la historia. |
| [Font](../../aspose.words/inlinestory/font) { get; } | Proporciona acceso al formato de fuente del carácter ancla de este objeto. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes) { get; } | Devuelve verdadero si este nodo tiene nodos secundarios. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite) { get; } | Devuelve verdadero ya que este nodo puede tener nodos secundarios. |
| [IsDeleteRevision](../../aspose.words/inlinestory/isdeleterevision) { get; } | Devuelve verdadero si este objeto se eliminó en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [IsInsertRevision](../../aspose.words/inlinestory/isinsertrevision) { get; } | Devuelve verdadero si este objeto se insertó en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [IsMoveFromRevision](../../aspose.words/inlinestory/ismovefromrevision) { get; } | Devoluciones **verdadero** si este objeto se movió (eliminó) en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [IsMoveToRevision](../../aspose.words/inlinestory/ismovetorevision) { get; } | Devoluciones **verdadero** si este objeto se movió (insertó) en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [LastChild](../../aspose.words/compositenode/lastchild) { get; } | Obtiene el último hijo del nodo. |
| [LastParagraph](../../aspose.words/inlinestory/lastparagraph) { get; } | Obtiene el último párrafo de la historia. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | Obtiene el nodo que sigue inmediatamente a este nodo. |
| abstract [NodeType](../../aspose.words/node/nodetype) { get; } | Obtiene el tipo de este nodo. |
| [Paragraphs](../../aspose.words/inlinestory/paragraphs) { get; } | Obtiene una colección de párrafos que son hijos inmediatos de la historia. |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | Obtiene el padre inmediato de este nodo. |
| [ParentParagraph](../../aspose.words/inlinestory/parentparagraph) { get; } | Recupera el padre[`Paragraph`](../paragraph) de este nodo. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | Obtiene el nodo inmediatamente anterior a este nodo. |
| [Range](../../aspose.words/node/range) { get; } | Devuelve un **Rango** objeto que representa la parte de un documento que está contenido en este nodo. |
| abstract [StoryType](../../aspose.words/inlinestory/storytype) { get; } | Devuelve el tipo de historia. |
| [Tables](../../aspose.words/inlinestory/tables) { get; } | Obtiene una colección de tablas que son elementos secundarios inmediatos de la historia. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| abstract [Accept](../../aspose.words/node/accept)(DocumentVisitor) | Acepta un visitante. |
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
| [RemoveChild](../../aspose.words/compositenode/removechild)(Node) | Elimina el nodo secundario especificado. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags)() | Elimina todo[`SmartTag`](../../aspose.words.markup/smarttag) nodos descendientes del nodo actual. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes)(string) | Selecciona una lista de nodos que coinciden con la expresión XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode)(string) | Selecciona el primer nodo que coincide con la expresión XPath. |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | Exporta el contenido del nodo a una cadena en el formato especificado. |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | Exporta el contenido del nodo a una cadena utilizando las opciones de guardado especificadas. |

### Observaciones

**Historia en línea** es un contenedor para nodos a nivel de bloque[`Paragraph`](../paragraph) y[`Table`](../../aspose.words.tables/table).

Las clases que se derivan de **Historia en línea** son nodos de nivel en línea que pueden contener su propio texto (párrafos y tablas). por ejemplo, un **Comentario** nodo contiene el texto de un comentario y un **Nota** contiene el texto de una nota al pie.

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

Muestra cómo insertar y personalizar notas al pie.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Agregue texto y haga referencia a él con una nota al pie. Esta nota al pie colocará una pequeña referencia en superíndice
// marca después del texto al que hace referencia y crea una entrada debajo del texto del cuerpo principal en la parte inferior de la página.
// Esta entrada contendrá la marca de referencia de la nota al pie y el texto de referencia,
// que pasaremos al método "InsertFootnote" del generador de documentos.
builder.Write("Main body text.");
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// Si esta propiedad se establece en "verdadero", entonces la marca de referencia de nuestra nota al pie
// será su índice entre todas las notas a pie de página de la sección.
// Esta es la primera nota al pie, por lo que la marca de referencia será "1".
Assert.True(footnote.IsAuto);

// Podemos mover el generador de documentos dentro de la nota al pie para editar su texto de referencia. 
builder.MoveTo(footnote.FirstParagraph);
builder.Write(" More text added by a DocumentBuilder.");
builder.MoveToDocumentEnd();

Assert.AreEqual("\u0002 Footnote text. More text added by a DocumentBuilder.", footnote.GetText().Trim());

builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// Podemos establecer una marca de referencia personalizada que utilizará la nota al pie en lugar de su número de índice.
footnote.ReferenceMark = "RefMark";

Assert.False(footnote.IsAuto);

// Un marcador con el indicador "IsAuto" establecido en verdadero seguirá mostrando su índice real
// incluso si los marcadores anteriores muestran marcas de referencia personalizadas, la marca de referencia de este marcador será un "3".
builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

Assert.True(footnote.IsAuto);

doc.Save(ArtifactsDir + "InlineStory.AddFootnote.docx");
```

### Ver también

* class [CompositeNode](../compositenode)
* espacio de nombres [Aspose.Words](../../aspose.words)
* asamblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
