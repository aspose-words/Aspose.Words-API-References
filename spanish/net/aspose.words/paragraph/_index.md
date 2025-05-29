---
title: Paragraph Class
linktitle: Paragraph
articleTitle: Paragraph
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Paragraph para administrar y formatear párrafos de texto sin esfuerzo, mejorando sus capacidades de procesamiento de documentos.
type: docs
weight: 5120
url: /es/net/aspose.words/paragraph/
---
## Paragraph class

Representa un párrafo de texto.

Para obtener más información, visite el[Trabajar con párrafos](https://docs.aspose.com/words/net/working-with-paragraphs/) Artículo de documentación.

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
| [BreakIsStyleSeparator](../../aspose.words/paragraph/breakisstyleseparator/) { get; } | Verdadero si este salto de párrafo es un separador de estilos. Un separador de estilos permite que un párrafo conste de partes con diferentes estilos de párrafo. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Obtiene el número de hijos inmediatos de este nodo. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Especifica un identificador de nodo personalizado. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Obtiene el documento al que pertenece este nodo. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Obtiene el primer hijo del nodo. |
| [FrameFormat](../../aspose.words/paragraph/frameformat/) { get; } | Proporciona acceso a las propiedades de formato del marco. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Devuelve`verdadero` si este nodo tiene nodos secundarios. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Devuelve`verdadero` ya que este nodo puede tener nodos secundarios. |
| [IsDeleteRevision](../../aspose.words/paragraph/isdeleterevision/) { get; } | Devuelve verdadero si este objeto se eliminó en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [IsEndOfCell](../../aspose.words/paragraph/isendofcell/) { get; } | Verdadero si este párrafo es el último párrafo de un[`Cell`](../../aspose.words.tables/cell/) ; falso en caso contrario. |
| [IsEndOfDocument](../../aspose.words/paragraph/isendofdocument/) { get; } | Verdadero si este párrafo es el último párrafo de la última sección del documento. |
| [IsEndOfHeaderFooter](../../aspose.words/paragraph/isendofheaderfooter/) { get; } | Verdadero si este párrafo es el último párrafo del[`HeaderFooter`](../headerfooter/) (historia del texto principal) de una[`Section`](../section/) ; falso en caso contrario. |
| [IsEndOfSection](../../aspose.words/paragraph/isendofsection/) { get; } | Verdadero si este párrafo es el último párrafo del[`Body`](../body/) (historia del texto principal) de una[`Section`](../section/) ; falso en caso contrario. |
| [IsFormatRevision](../../aspose.words/paragraph/isformatrevision/) { get; } | Devuelve verdadero si se cambió el formato del objeto en Microsoft Word mientras estaba habilitado el seguimiento de cambios. |
| [IsInCell](../../aspose.words/paragraph/isincell/) { get; } | Verdadero si este párrafo es un hijo inmediato de[`Cell`](../../aspose.words.tables/cell/) ; falso en caso contrario. |
| [IsInsertRevision](../../aspose.words/paragraph/isinsertrevision/) { get; } | Devuelve verdadero si este objeto se insertó en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [IsListItem](../../aspose.words/paragraph/islistitem/) { get; } | Verdadero cuando el párrafo es un elemento de una lista numerada o con viñetas en la revisión original. |
| [IsMoveFromRevision](../../aspose.words/paragraph/ismovefromrevision/) { get; } | Devuelve`verdadero` Si este objeto se movió (eliminó) en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [IsMoveToRevision](../../aspose.words/paragraph/ismovetorevision/) { get; } | Devuelve`verdadero` Si este objeto se movió (insertó) en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Obtiene el último hijo del nodo. |
| [ListFormat](../../aspose.words/paragraph/listformat/) { get; } | Proporciona acceso a las propiedades de formato de lista del párrafo. |
| [ListLabel](../../aspose.words/paragraph/listlabel/) { get; } | Obtiene un[`ListLabel`](./listlabel/)objeto que proporciona acceso al valor de numeración de lista y formato para este párrafo. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Obtiene el nodo inmediatamente siguiente a este nodo. |
| override [NodeType](../../aspose.words/paragraph/nodetype/) { get; } | DevuelveParagraph . |
| [ParagraphBreakFont](../../aspose.words/paragraph/paragraphbreakfont/) { get; } | Proporciona acceso al formato de fuente del carácter de salto de párrafo. |
| [ParagraphFormat](../../aspose.words/paragraph/paragraphformat/) { get; } | Proporciona acceso a las propiedades de formato de párrafo. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Obtiene el padre inmediato de este nodo. |
| [ParentSection](../../aspose.words/paragraph/parentsection/) { get; } | Recupera el padre[`Section`](../section/) del párrafo. |
| [ParentStory](../../aspose.words/paragraph/parentstory/) { get; } | Recupera la historia a nivel de sección principal que se puede[`Body`](../body/) o[`HeaderFooter`](../headerfooter/) . |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Obtiene el nodo inmediatamente anterior a este nodo. |
| [Range](../../aspose.words/node/range/) { get; } | Devuelve un[`Range`](../range/)objeto que representa la porción de un documento que está contenida en este nodo. |
| [Runs](../../aspose.words/paragraph/runs/) { get; } | Proporciona acceso a la colección escrita de fragmentos de texto dentro del párrafo. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| override [Accept](../../aspose.words/paragraph/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Acepta un visitante. |
| override [AcceptEnd](../../aspose.words/paragraph/acceptend/)(*[DocumentVisitor](../documentvisitor/)*) | Acepta a un visitante por visitar el final del párrafo del documento. |
| override [AcceptStart](../../aspose.words/paragraph/acceptstart/)(*[DocumentVisitor](../documentvisitor/)*) | Acepta a un visitante por visitar el inicio del párrafo del documento. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | Agrega el nodo especificado al final de la lista de nodos secundarios para este nodo. |
| [AppendField](../../aspose.words/paragraph/appendfield/#appendfield_1)(*string*) | Agrega un campo a este párrafo. |
| [AppendField](../../aspose.words/paragraph/appendfield/#appendfield)(*[FieldType](../../aspose.words.fields/fieldtype/), bool*) | Agrega un campo a este párrafo. |
| [AppendField](../../aspose.words/paragraph/appendfield/#appendfield_2)(*string, string*) | Agrega un campo a este párrafo. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Crea un duplicado del nodo. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Crea un navegador que puede utilizarse para recorrer y leer nodos. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | Obtiene el primer ancestro del especificado[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Obtiene el primer ancestro del tipo de objeto especificado. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../nodetype/), int, bool*) | Devuelve un nodo secundario N que coincide con el tipo especificado. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../nodetype/), bool*) | Devuelve una colección activa de nodos secundarios que coinciden con el tipo especificado. |
| [GetEffectiveTabStops](../../aspose.words/paragraph/geteffectivetabstops/)() | Devuelve una matriz de todas las tabulaciones aplicadas a este párrafo, incluidas las aplicadas indirectamente por estilos o listas. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Proporciona soporte para cada iteración de estilo sobre los nodos secundarios de este nodo. |
| override [GetText](../../aspose.words/paragraph/gettext/)() | Obtiene el texto de este párrafo incluido el carácter de final de párrafo. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../node/)*) | Devuelve el índice del nodo secundario especificado en la matriz de nodos secundarios. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(*T, [Node](../node/)*) | Inserta el nodo especificado inmediatamente después del nodo de referencia especificado. |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(*T, [Node](../node/)*) | Inserta el nodo especificado inmediatamente antes del nodo de referencia especificado. |
| [InsertField](../../aspose.words/paragraph/insertfield/#insertfield_1)(*string, [Node](../node/), bool*) | Inserta un campo en este párrafo. |
| [InsertField](../../aspose.words/paragraph/insertfield/#insertfield)(*[FieldType](../../aspose.words.fields/fieldtype/), bool, [Node](../node/), bool*) | Inserta un campo en este párrafo. |
| [InsertField](../../aspose.words/paragraph/insertfield/#insertfield_2)(*string, string, [Node](../node/), bool*) | Inserta un campo en este párrafo. |
| [JoinRunsWithSameFormatting](../../aspose.words/paragraph/joinrunswithsameformatting/)() | Une líneas con el mismo formato en el párrafo. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../node/)*) | Obtiene el siguiente nodo según el algoritmo de recorrido del árbol de preorden. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(*T*) | Agrega el nodo especificado al comienzo de la lista de nodos secundarios para este nodo. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../node/)*) | Obtiene el nodo anterior según el algoritmo de recorrido del árbol de preorden. |
| [Remove](../../aspose.words/node/remove/)() | Se elimina a sí mismo del padre. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Elimina todos los nodos secundarios del nodo actual. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(*T*) | Elimina el nodo secundario especificado. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Elimina todo[`SmartTag`](../../aspose.words.markup/smarttag/) nodos descendientes del nodo actual. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | Selecciona una lista de nodos que coinciden con la expresión XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | Selecciona el primer[`Node`](../node/) que coincide con la expresión XPath. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../saveformat/)*) | Exporta el contenido del nodo en una cadena en el formato especificado. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Exporta el contenido del nodo en una cadena utilizando las opciones de guardado especificadas. |

## Observaciones

`Paragraph` es un nodo a nivel de bloque y puede ser un hijo de clases derivadas de [`Story`](../story/) o[`InlineStory`](../inlinestory/).

`Paragraph` Puede contener cualquier número de nodos y marcadores de nivel en línea.

La lista completa de nodos secundarios que pueden aparecer dentro de un párrafo consta de [`BookmarkStart`](../bookmarkstart/) ,[`BookmarkEnd`](../bookmarkend/) , [`FieldStart`](../../aspose.words.fields/fieldstart/) ,[`FieldSeparator`](../../aspose.words.fields/fieldseparator/) , [`FieldEnd`](../../aspose.words.fields/fieldend/) ,[`FormField`](../../aspose.words.fields/formfield/) , [`Comment`](../comment/) ,[`Footnote`](../../aspose.words.notes/footnote/) , [`Run`](../run/) ,[`SpecialChar`](../specialchar/) , [`Shape`](../../aspose.words.drawing/shape/) ,[`GroupShape`](../../aspose.words.drawing/groupshape/) , [`SmartTag`](../../aspose.words.markup/smarttag/).

Un párrafo válido en Microsoft Word siempre termina con un carácter de salto de párrafo y un párrafo válido mínimo consta solo de un salto de párrafo. El`Paragraph` La clase agrega automáticamente el carácter de salto de párrafo apropiado al final y este carácter no es parte de los nodos secundarios de la clase.`Paragraph` , por lo tanto a`Paragraph` Puede estar vacío.

No incluya el final del párrafo[`ParagraphBreak`](../controlchar/paragraphbreak/) o fin de celda[`Cell`](../controlchar/cell/) caracteres dentro del texto del párrafo, ya que podría hacer que el párrafo sea inválido cuando el documento se abra en Microsoft Word.

## Ejemplos

Muestra cómo construir un documento Aspose.Words a mano.

```csharp
Document doc = new Document();

// Un documento en blanco contiene una sección, un cuerpo y un párrafo.
// Llama al método "RemoveAllChildren" para eliminar todos esos nodos,
// y terminar con un nodo de documento sin hijos.
doc.RemoveAllChildren();

//Este documento ahora no tiene nodos secundarios compuestos a los que podamos agregar contenido.
// Si deseamos editarlo, necesitaremos volver a llenar su colección de nodos.
// Primero, cree una nueva sección y luego añádala como un elemento secundario al nodo del documento raíz.
Section section = new Section(doc);
doc.AppendChild(section);

// Establezca algunas propiedades de configuración de página para la sección.
section.PageSetup.SectionStart = SectionStart.NewPage;
section.PageSetup.PaperSize = PaperSize.Letter;

// Una sección necesita un cuerpo, que contendrá y mostrará todo su contenido.
// en la página entre el encabezado y el pie de página de la sección.
Body body = new Body(doc);
section.AppendChild(body);

// Cree un párrafo, establezca algunas propiedades de formato y luego añádalo como elemento secundario al cuerpo.
Paragraph para = new Paragraph(doc);

para.ParagraphFormat.StyleName = "Heading 1";
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;

body.AppendChild(para);

// Finalmente, agrega algo de contenido para completar el documento. Crea una ejecución.
// establece su apariencia y contenido, y luego lo agrega como un elemento secundario al párrafo.
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
