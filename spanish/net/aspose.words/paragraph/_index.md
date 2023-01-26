---
title: Paragraph
second_title: Referencia de API de Aspose.Words para .NET
description: Representa un párrafo de texto.
type: docs
weight: 4150
url: /es/net/aspose.words/paragraph/
---
## Paragraph class

Representa un párrafo de texto.

```csharp
public class Paragraph : CompositeNode
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [Paragraph](paragraph/)(DocumentBase) | Inicializa una nueva instancia del **Párrafo** clase. |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [BreakIsStyleSeparator](../../aspose.words/paragraph/breakisstyleseparator/) { get; } | Verdadero si este salto de párrafo es un separador de estilo. Un separador de estilo permite que un párrafo conste de partes que tienen diferentes estilos de párrafo. |
| [ChildNodes](../../aspose.words/compositenode/childnodes/) { get; } | Obtiene todos los nodos secundarios inmediatos de este nodo. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Obtiene el número de hijos inmediatos de este nodo. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Especifica el identificador de nodo personalizado. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Obtiene el documento al que pertenece este nodo. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Obtiene el primer hijo del nodo. |
| [FrameFormat](../../aspose.words/paragraph/frameformat/) { get; } | Proporciona acceso a las propiedades de formato de párrafo. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Devuelve verdadero si este nodo tiene nodos secundarios. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Devuelve verdadero ya que este nodo puede tener nodos secundarios. |
| [IsDeleteRevision](../../aspose.words/paragraph/isdeleterevision/) { get; } | Devuelve verdadero si este objeto se eliminó en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [IsEndOfCell](../../aspose.words/paragraph/isendofcell/) { get; } | Verdadero si este párrafo es el último párrafo de un[`Cell`](../../aspose.words.tables/cell/) ; falso en caso contrario. |
| [IsEndOfDocument](../../aspose.words/paragraph/isendofdocument/) { get; } | Verdadero si este párrafo es el último párrafo de la última sección del documento. |
| [IsEndOfHeaderFooter](../../aspose.words/paragraph/isendofheaderfooter/) { get; } | Verdadero si este párrafo es el último párrafo del **EncabezadoPie de página** (historia del texto principal) de un **Sección** ; falso en caso contrario. |
| [IsEndOfSection](../../aspose.words/paragraph/isendofsection/) { get; } | Verdadero si este párrafo es el último párrafo del **Cuerpo** (historia del texto principal) de un **Sección** ; falso en caso contrario. |
| [IsFormatRevision](../../aspose.words/paragraph/isformatrevision/) { get; } | Devuelve verdadero si se cambió el formato del objeto en Microsoft Word mientras estaba habilitado el seguimiento de cambios. |
| [IsInCell](../../aspose.words/paragraph/isincell/) { get; } | Verdadero si este párrafo es un hijo inmediato de[`Cell`](../../aspose.words.tables/cell/) ; falso en caso contrario. |
| [IsInsertRevision](../../aspose.words/paragraph/isinsertrevision/) { get; } | Devuelve verdadero si este objeto se insertó en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [IsListItem](../../aspose.words/paragraph/islistitem/) { get; } | Verdadero cuando el párrafo es un elemento en una lista numerada o con viñetas en la revisión original. |
| [IsMoveFromRevision](../../aspose.words/paragraph/ismovefromrevision/) { get; } | Devoluciones **verdadero** si este objeto se movió (eliminó) en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [IsMoveToRevision](../../aspose.words/paragraph/ismovetorevision/) { get; } | Devoluciones **verdadero** si este objeto se movió (insertó) en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Obtiene el último hijo del nodo. |
| [ListFormat](../../aspose.words/paragraph/listformat/) { get; } | Proporciona acceso a las propiedades de formato de lista del párrafo. |
| [ListLabel](../../aspose.words/paragraph/listlabel/) { get; } | Obtiene un[`ListLabel`](./listlabel/) objeto que proporciona acceso al valor de numeración de la lista y formato para este párrafo. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Obtiene el nodo que sigue inmediatamente a este nodo. |
| override [NodeType](../../aspose.words/paragraph/nodetype/) { get; } | Devoluciones **NodeType.Paragraph** . |
| [ParagraphBreakFont](../../aspose.words/paragraph/paragraphbreakfont/) { get; } | Proporciona acceso al formato de fuente del carácter de salto de párrafo. |
| [ParagraphFormat](../../aspose.words/paragraph/paragraphformat/) { get; } | Proporciona acceso a las propiedades de formato de párrafo. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Obtiene el padre inmediato de este nodo. |
| [ParentSection](../../aspose.words/paragraph/parentsection/) { get; } | Recupera el padre[`Section`](../section/) del párrafo. |
| [ParentStory](../../aspose.words/paragraph/parentstory/) { get; } | Recupera la historia principal a nivel de sección que se puede[`Body`](../body/) o[`HeaderFooter`](../headerfooter/) . |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Obtiene el nodo inmediatamente anterior a este nodo. |
| [Range](../../aspose.words/node/range/) { get; } | Devuelve un **Rango** objeto que representa la parte de un documento que está contenido en este nodo. |
| [Runs](../../aspose.words/paragraph/runs/) { get; } | Proporciona acceso a la colección mecanografiada de fragmentos de texto dentro del párrafo. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| override [Accept](../../aspose.words/paragraph/accept/)(DocumentVisitor) | Acepta un visitante. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(Node) | Agrega el nodo especificado al final de la lista de nodos secundarios para este nodo. |
| [AppendField](../../aspose.words/paragraph/appendfield/#appendfield_1)(string) | Agrega un campo a este párrafo. |
| [AppendField](../../aspose.words/paragraph/appendfield/#appendfield)(FieldType, bool) | Agrega un campo a este párrafo. |
| [AppendField](../../aspose.words/paragraph/appendfield/#appendfield_2)(string, string) | Agrega un campo a este párrafo. |
| [Clone](../../aspose.words/node/clone/)(bool) | Crea un duplicado del nodo. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Reservado para uso del sistema. IXPathNavigable. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Obtiene el primer ancestro del especificado[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Obtiene el primer ancestro del tipo de objeto especificado. |
| [GetChild](../../aspose.words/compositenode/getchild/)(NodeType, int, bool) | Devuelve un enésimo nodo secundario que coincide con el tipo especificado. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(NodeType, bool) | Devuelve una colección activa de nodos secundarios que coinciden con el tipo especificado. |
| [GetEffectiveTabStops](../../aspose.words/paragraph/geteffectivetabstops/)() | Devuelve una matriz de todas las tabulaciones aplicadas a este párrafo, incluidas las aplicadas indirectamente por estilos o listas. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Proporciona soporte para la iteración de cada estilo sobre los nodos secundarios de este nodo. |
| override [GetText](../../aspose.words/paragraph/gettext/)() | Obtiene el texto de este párrafo, incluido el carácter de fin de párrafo. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(Node) | Devuelve el índice del nodo secundario especificado en la matriz de nodos secundarios. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(Node, Node) | Inserta el nodo especificado inmediatamente después del nodo de referencia especificado. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(Node, Node) | Inserta el nodo especificado inmediatamente antes del nodo de referencia especificado. |
| [InsertField](../../aspose.words/paragraph/insertfield/#insertfield_1)(string, Node, bool) | Inserta un campo en este párrafo. |
| [InsertField](../../aspose.words/paragraph/insertfield/#insertfield)(FieldType, bool, Node, bool) | Inserta un campo en este párrafo. |
| [InsertField](../../aspose.words/paragraph/insertfield/#insertfield_2)(string, string, Node, bool) | Inserta un campo en este párrafo. |
| [JoinRunsWithSameFormatting](../../aspose.words/paragraph/joinrunswithsameformatting/)() | Une ejecuciones con el mismo formato en el párrafo. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Obtiene el siguiente nodo de acuerdo con el algoritmo de recorrido del árbol de pedido previo. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(Node) | Agrega el nodo especificado al principio de la lista de nodos secundarios para este nodo. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Obtiene el nodo anterior de acuerdo con el algoritmo de recorrido del árbol de pedido previo. |
| [Remove](../../aspose.words/node/remove/)() | Se elimina a sí mismo del padre. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Elimina todos los nodos secundarios del nodo actual. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(Node) | Elimina el nodo secundario especificado. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Elimina todo[`SmartTag`](../../aspose.words.markup/smarttag/) nodos descendientes del nodo actual. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(string) | Selecciona una lista de nodos que coinciden con la expresión XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | Selecciona el primer nodo que coincide con la expresión XPath. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Exporta el contenido del nodo a una cadena en el formato especificado. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Exporta el contenido del nodo a una cadena utilizando las opciones de guardado especificadas. |

### Observaciones

`Paragraph` es un nodo a nivel de bloque y puede ser un hijo de clases derivadas de [`Story`](../story/) o[`InlineStory`](../inlinestory/).

`Paragraph` puede contener cualquier número de nodos y marcadores de nivel en línea.

La lista completa de nodos secundarios que pueden aparecer dentro de un párrafo consta de [`BookmarkStart`](../bookmarkstart/) ,[`BookmarkEnd`](../bookmarkend/) , [`FieldStart`](../../aspose.words.fields/fieldstart/) ,[`FieldSeparator`](../../aspose.words.fields/fieldseparator/) , [`FieldEnd`](../../aspose.words.fields/fieldend/) ,[`FormField`](../../aspose.words.fields/formfield/) , [`Comment`](../comment/) ,[`Footnote`](../../aspose.words.notes/footnote/) , [`Run`](../run/) ,[`SpecialChar`](../specialchar/) , [`Shape`](../../aspose.words.drawing/shape/) ,[`GroupShape`](../../aspose.words.drawing/groupshape/) , [`SmartTag`](../../aspose.words.markup/smarttag/).

Un párrafo válido en Microsoft Word siempre termina con un carácter de salto de párrafo y un párrafo válido mínimo consiste solo en un salto de párrafo. los **Párrafo** La clase agrega automáticamente el carácter de salto de párrafo apropiado al final y este carácter no forma parte de los nodos secundarios de la **Párrafo** , por lo tanto a **Párrafo** puede estar vacío.

No incluir el final del párrafo.[`ControlChar.ParagraphBreak`](../controlchar/paragraphbreak/) o final de celda[`ControlChar.Célula`](../controlchar/cell/) caracteres dentro del texto de el párrafo, ya que podría invalidar el párrafo cuando se abre el documento en Microsoft Word.

### Ejemplos

Muestra cómo construir un documento de Aspose.Words a mano.

```csharp
Document doc = new Document();

// Un documento en blanco contiene una sección, un cuerpo y un párrafo.
// Llame al método "RemoveAllChildren" para eliminar todos esos nodos,
// y terminar con un nodo de documento sin hijos.
doc.RemoveAllChildren();

// Este documento ahora no tiene nodos secundarios compuestos a los que podamos agregar contenido.
// Si deseamos editarlo, necesitaremos volver a llenar su colección de nodos.
// Primero, cree una nueva sección y luego agréguela como elemento secundario al nodo del documento raíz.
Section section = new Section(doc);
doc.AppendChild(section);

// Establecer algunas propiedades de configuración de página para la sección.
section.PageSetup.SectionStart = SectionStart.NewPage;
section.PageSetup.PaperSize = PaperSize.Letter;

// Una sección necesita un cuerpo, que contendrá y mostrará todo su contenido
// en la página entre el encabezado y el pie de página de la sección.
Body body = new Body(doc);
section.AppendChild(body);

// Cree un párrafo, establezca algunas propiedades de formato y luego agréguelo como elemento secundario al cuerpo.
Paragraph para = new Paragraph(doc);

para.ParagraphFormat.StyleName = "Heading 1";
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;

body.AppendChild(para);

// Finalmente, agregue algo de contenido para hacer el documento. Crear una carrera,
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

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
