---
title: Paragraph Class
linktitle: Paragraph
articleTitle: Paragraph
second_title: Aspose.Words para .NET
description: Aspose.Words.Paragraph clase. Representa un párrafo de texto en C#.
type: docs
weight: 4390
url: /es/net/aspose.words/paragraph/
---
## Paragraph class

Representa un párrafo de texto.

Para obtener más información, visite el[Trabajar con párrafos](https://docs.aspose.com/words/net/working-with-paragraphs/) artículo de documentación.

```csharp
public class Paragraph : CompositeNode
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [Paragraph](paragraph/)(*[DocumentBase](../documentbase/)*) | Inicializa una nueva instancia del`Paragraph` clase. |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [BreakIsStyleSeparator](../../aspose.words/paragraph/breakisstyleseparator/) { get; } | Verdadero si este salto de párrafo es un separador de estilo. Un separador de estilo permite que un párrafo esté formado por partes que tienen diferentes estilos de párrafo. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Obtiene el número de hijos inmediatos de este nodo. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Especifica el identificador de nodo personalizado. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Obtiene el documento al que pertenece este nodo. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Obtiene el primer hijo del nodo. |
| [FrameFormat](../../aspose.words/paragraph/frameformat/) { get; } | Proporciona acceso a las propiedades de formato del marco. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Devoluciones`verdadero` si este nodo tiene nodos secundarios. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Devoluciones`verdadero` ya que este nodo puede tener nodos secundarios. |
| [IsDeleteRevision](../../aspose.words/paragraph/isdeleterevision/) { get; } | Devuelve verdadero si este objeto se eliminó en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [IsEndOfCell](../../aspose.words/paragraph/isendofcell/) { get; } | Verdadero si este párrafo es el último párrafo de un[`Cell`](../../aspose.words.tables/cell/) ; falso en caso contrario. |
| [IsEndOfDocument](../../aspose.words/paragraph/isendofdocument/) { get; } | Verdadero si este párrafo es el último párrafo de la última sección del documento. |
| [IsEndOfHeaderFooter](../../aspose.words/paragraph/isendofheaderfooter/) { get; } | Verdadero si este párrafo es el último párrafo del[`HeaderFooter`](../headerfooter/) (historia del texto principal) de un[`Section`](../section/) ; falso en caso contrario. |
| [IsEndOfSection](../../aspose.words/paragraph/isendofsection/) { get; } | Verdadero si este párrafo es el último párrafo del[`Body`](../body/) (historia del texto principal) de un[`Section`](../section/) ; falso en caso contrario. |
| [IsFormatRevision](../../aspose.words/paragraph/isformatrevision/) { get; } | Devuelve verdadero si se cambió el formato del objeto en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [IsInCell](../../aspose.words/paragraph/isincell/) { get; } | Verdadero si este párrafo es hijo inmediato de[`Cell`](../../aspose.words.tables/cell/) ; falso en caso contrario. |
| [IsInsertRevision](../../aspose.words/paragraph/isinsertrevision/) { get; } | Devuelve verdadero si este objeto se insertó en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [IsListItem](../../aspose.words/paragraph/islistitem/) { get; } | Verdadero cuando el párrafo es un elemento en una lista numerada o con viñetas en la revisión original. |
| [IsMoveFromRevision](../../aspose.words/paragraph/ismovefromrevision/) { get; } | Devoluciones`verdadero` si este objeto se movió (eliminó) en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [IsMoveToRevision](../../aspose.words/paragraph/ismovetorevision/) { get; } | Devoluciones`verdadero` si este objeto se movió (insertó) en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Obtiene el último hijo del nodo. |
| [ListFormat](../../aspose.words/paragraph/listformat/) { get; } | Proporciona acceso a las propiedades de formato de lista del párrafo. |
| [ListLabel](../../aspose.words/paragraph/listlabel/) { get; } | Obtiene un[`ListLabel`](./listlabel/)objeto que proporciona acceso al valor de numeración de la lista y al formato para este párrafo. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Obtiene el nodo que sigue inmediatamente a este nodo. |
| override [NodeType](../../aspose.words/paragraph/nodetype/) { get; } | DevolucionesParagraph . |
| [ParagraphBreakFont](../../aspose.words/paragraph/paragraphbreakfont/) { get; } | Proporciona acceso al formato de fuente del carácter de salto de párrafo. |
| [ParagraphFormat](../../aspose.words/paragraph/paragraphformat/) { get; } | Proporciona acceso a las propiedades de formato de párrafo. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Obtiene el padre inmediato de este nodo. |
| [ParentSection](../../aspose.words/paragraph/parentsection/) { get; } | Recupera el padre[`Section`](../section/) del párrafo. |
| [ParentStory](../../aspose.words/paragraph/parentstory/) { get; } | Recupera la historia a nivel de sección principal que se puede[`Body`](../body/) o[`HeaderFooter`](../headerfooter/) . |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Obtiene el nodo inmediatamente anterior a este nodo. |
| [Range](../../aspose.words/node/range/) { get; } | Devuelve un[`Range`](../range/) objeto que representa la parte de un documento contenido en este nodo. |
| [Runs](../../aspose.words/paragraph/runs/) { get; } | Proporciona acceso a la colección mecanografiada de fragmentos de texto dentro del párrafo. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| override [Accept](../../aspose.words/paragraph/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Acepta un visitante. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(*[Node](../node/)*) | Agrega el nodo especificado al final de la lista de nodos secundarios para este nodo. |
| [AppendField](../../aspose.words/paragraph/appendfield/#appendfield_1)(*string*) | Agrega un campo a este párrafo. |
| [AppendField](../../aspose.words/paragraph/appendfield/#appendfield)(*[FieldType](../../aspose.words.fields/fieldtype/), bool*) | Agrega un campo a este párrafo. |
| [AppendField](../../aspose.words/paragraph/appendfield/#appendfield_2)(*string, string*) | Agrega un campo a este párrafo. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Crea un duplicado del nodo. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Crea un navegador que se puede utilizar para atravesar y leer nodos. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | Obtiene el primer ancestro del especificado[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Obtiene el primer antepasado del tipo de objeto especificado. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../nodetype/), int, bool*) | Devuelve un enésimo nodo secundario que coincide con el tipo especificado. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../nodetype/), bool*) | Devuelve una colección activa de nodos secundarios que coinciden con el tipo especificado. |
| [GetEffectiveTabStops](../../aspose.words/paragraph/geteffectivetabstops/)() | Devuelve una matriz de todas las tabulaciones aplicadas a este párrafo, incluidas las aplicadas indirectamente mediante estilos o listas. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Proporciona soporte para cada iteración de estilo sobre los nodos secundarios de este nodo. |
| override [GetText](../../aspose.words/paragraph/gettext/)() | Obtiene el texto de este párrafo, incluido el carácter de final de párrafo. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../node/)*) | Devuelve el índice del nodo secundario especificado en la matriz de nodos secundarios. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(*[Node](../node/), [Node](../node/)*) | Inserta el nodo especificado inmediatamente después del nodo de referencia especificado. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(*[Node](../node/), [Node](../node/)*) | Inserta el nodo especificado inmediatamente antes del nodo de referencia especificado. |
| [InsertField](../../aspose.words/paragraph/insertfield/#insertfield_1)(*string, [Node](../node/), bool*) | Inserta un campo en este párrafo. |
| [InsertField](../../aspose.words/paragraph/insertfield/#insertfield)(*[FieldType](../../aspose.words.fields/fieldtype/), bool, [Node](../node/), bool*) | Inserta un campo en este párrafo. |
| [InsertField](../../aspose.words/paragraph/insertfield/#insertfield_2)(*string, string, [Node](../node/), bool*) | Inserta un campo en este párrafo. |
| [JoinRunsWithSameFormatting](../../aspose.words/paragraph/joinrunswithsameformatting/)() | Une ejecuciones con el mismo formato en el párrafo. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../node/)*) | Obtiene el siguiente nodo según el algoritmo transversal del árbol de pedidos anticipados. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(*[Node](../node/)*) | Agrega el nodo especificado al principio de la lista de nodos secundarios para este nodo. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../node/)*) | Obtiene el nodo anterior según el algoritmo transversal del árbol de pedidos anticipados. |
| [Remove](../../aspose.words/node/remove/)() | Se elimina del padre. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Elimina todos los nodos secundarios del nodo actual. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(*[Node](../node/)*) | Elimina el nodo secundario especificado. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Elimina todo[`SmartTag`](../../aspose.words.markup/smarttag/)nodos descendientes del nodo actual. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | Selecciona una lista de nodos que coinciden con la expresión XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | Selecciona el primero[`Node`](../node/) que coincide con la expresión XPath. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../saveformat/)*) | Exporta el contenido del nodo a una cadena en el formato especificado. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Exporta el contenido del nodo a una cadena usando las opciones de guardado especificadas. |

## Observaciones

`Paragraph` es un nodo a nivel de bloque y puede ser hijo de clases derivadas de [`Story`](../story/) o[`InlineStory`](../inlinestory/).

`Paragraph` puede contener cualquier número de nodos y marcadores de nivel en línea.

La lista completa de nodos secundarios que pueden aparecer dentro de un párrafo consta de [`BookmarkStart`](../bookmarkstart/) ,[`BookmarkEnd`](../bookmarkend/) , [`FieldStart`](../../aspose.words.fields/fieldstart/) ,[`FieldSeparator`](../../aspose.words.fields/fieldseparator/) , [`FieldEnd`](../../aspose.words.fields/fieldend/) ,[`FormField`](../../aspose.words.fields/formfield/) , [`Comment`](../comment/) ,[`Footnote`](../../aspose.words.notes/footnote/) , [`Run`](../run/) ,[`SpecialChar`](../specialchar/) , [`Shape`](../../aspose.words.drawing/shape/) ,[`GroupShape`](../../aspose.words.drawing/groupshape/) , [`SmartTag`](../../aspose.words.markup/smarttag/).

Un párrafo válido en Microsoft Word siempre termina con un carácter de salto de párrafo y un párrafo válido mínimo consta solo de un salto de párrafo. El`Paragraph` La clase agrega automáticamente el carácter de salto de párrafo apropiado al final y este carácter no forma parte de los nodos secundarios del`Paragraph` , por lo tanto a`Paragraph` puede estar vacío.

No incluya el final del párrafo.[`ParagraphBreak`](../controlchar/paragraphbreak/) o fin de celda[`Cell`](../controlchar/cell/) caracteres dentro del texto de el párrafo, ya que podría invalidar el párrafo cuando se abre el documento en Microsoft Word.

## Ejemplos

Muestra cómo construir un documento Aspose.Words a mano.

```csharp
Document doc = new Document();

// Un documento en blanco contiene una sección, un cuerpo y un párrafo.
// Llama al método "RemoveAllChildren" para eliminar todos esos nodos,
// y terminar con un nodo de documento sin hijos.
doc.RemoveAllChildren();

// Este documento ahora no tiene nodos secundarios compuestos a los que podamos agregar contenido.
// Si deseamos editarlo, necesitaremos volver a llenar su colección de nodos.
// Primero, crea una nueva sección y luego agrégala como secundaria al nodo del documento raíz.
Section section = new Section(doc);
doc.AppendChild(section);

// Establece algunas propiedades de configuración de página para la sección.
section.PageSetup.SectionStart = SectionStart.NewPage;
section.PageSetup.PaperSize = PaperSize.Letter;

// Una sección necesita un cuerpo, que contendrá y mostrará todo su contenido
// en la página entre el encabezado y el pie de página de la sección.
Body body = new Body(doc);
section.AppendChild(body);

// Crea un párrafo, establece algunas propiedades de formato y luego añádelo como elemento secundario al cuerpo.
Paragraph para = new Paragraph(doc);

para.ParagraphFormat.StyleName = "Heading 1";
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;

body.AppendChild(para);

// Finalmente, agrega algo de contenido para hacer el documento. Crea una carrera,
// establece su apariencia y contenido, y luego lo agrega como elemento secundario al párrafo.
Run run = new Run(doc);
run.Text = "Hello World!";
run.Font.Color = Color.Red;
para.AppendChild(run);

Assert.AreEqual("Hello World!", doc.GetText().Trim());

doc.Save(ArtifactsDir + "Section.CreateManually.docx");
```

### Ver también

* class [CompositeNode](../compositenode/)
* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
