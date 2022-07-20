---
title: Body
second_title: Referencia de API de Aspose.Words para .NET
description: Representa un contenedor para el texto principal de una sección.
type: docs
weight: 20
url: /es/net/aspose.words/body/
---
## Body class

Representa un contenedor para el texto principal de una sección.

```csharp
public class Body : Story
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [Body](body)(DocumentBase) | Inicializa una nueva instancia del **Cuerpo** clase. |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [ChildNodes](../../aspose.words/compositenode/childnodes) { get; } | Obtiene todos los nodos secundarios inmediatos de este nodo. |
| [Count](../../aspose.words/compositenode/count) { get; } | Obtiene el número de hijos inmediatos de este nodo. |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | Especifica el identificador de nodo personalizado. |
| virtual [Document](../../aspose.words/node/document) { get; } | Obtiene el documento al que pertenece este nodo. |
| [FirstChild](../../aspose.words/compositenode/firstchild) { get; } | Obtiene el primer hijo del nodo. |
| [FirstParagraph](../../aspose.words/story/firstparagraph) { get; } | Obtiene el primer párrafo de la historia. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes) { get; } | Devuelve verdadero si este nodo tiene nodos secundarios. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite) { get; } | Devuelve verdadero ya que este nodo puede tener nodos secundarios. |
| [LastChild](../../aspose.words/compositenode/lastchild) { get; } | Obtiene el último hijo del nodo. |
| [LastParagraph](../../aspose.words/story/lastparagraph) { get; } | Obtiene el último párrafo de la historia. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | Obtiene el nodo que sigue inmediatamente a este nodo. |
| override [NodeType](../../aspose.words/body/nodetype) { get; } | Devoluciones **Tipo de nodo.Cuerpo** . |
| [Paragraphs](../../aspose.words/story/paragraphs) { get; } | Obtiene una colección de párrafos que son hijos inmediatos de la historia. |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | Obtiene el padre inmediato de este nodo. |
| [ParentSection](../../aspose.words/body/parentsection) { get; } | Obtiene la sección principal de esta historia. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | Obtiene el nodo inmediatamente anterior a este nodo. |
| [Range](../../aspose.words/node/range) { get; } | Devuelve un **Rango** objeto que representa la parte de un documento que está contenido en este nodo. |
| [StoryType](../../aspose.words/story/storytype) { get; } | Obtiene el tipo de esta historia. |
| [Tables](../../aspose.words/story/tables) { get; } | Obtiene una colección de tablas que son elementos secundarios inmediatos de la historia. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| override [Accept](../../aspose.words/body/accept)(DocumentVisitor) | Acepta un visitante. |
| [AppendChild](../../aspose.words/compositenode/appendchild)(Node) | Agrega el nodo especificado al final de la lista de nodos secundarios para este nodo. |
| [AppendParagraph](../../aspose.words/story/appendparagraph)(string) | Un método abreviado que crea un[`Paragraph`](../paragraph) objeto con texto opcional y lo agrega al final de este objeto. |
| [Clone](../../aspose.words/node/clone)(bool) | Crea un duplicado del nodo. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator)() | Reservado para uso del sistema. IXPathNavigable. |
| [DeleteShapes](../../aspose.words/story/deleteshapes)() | Elimina todas las formas del texto de esta historia. |
| [EnsureMinimum](../../aspose.words/body/ensureminimum)() | Si el último elemento secundario no es un párrafo, crea y agrega un párrafo vacío. |
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

**Cuerpo** puede contener **Párrafo** y **Mesa** nodos secundarios.

**Cuerpo** es un nodo de nivel de sección y solo puede ser un hijo de **Sección** . Solo puede haber uno **Cuerpo** en un **Sección**.

Un mínimo válido **Cuerpo** debe contener al menos una **Párrafo**.

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

* class [Story](../story)
* espacio de nombres [Aspose.Words](../../aspose.words)
* asamblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
