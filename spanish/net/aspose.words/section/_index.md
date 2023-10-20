---
title: Section Class
linktitle: Section
articleTitle: Section
second_title: Aspose.Words para .NET
description: Aspose.Words.Section clase. Representa una única sección de un documento en C#.
type: docs
weight: 5730
url: /es/net/aspose.words/section/
---
## Section class

Representa una única sección de un documento.

Para obtener más información, visite el[Trabajar con secciones](https://docs.aspose.com/words/net/working-with-sections/) artículo de documentación.

```csharp
public sealed class Section : CompositeNode
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [Section](section/)(*[DocumentBase](../documentbase/)*) | Inicializa una nueva instancia de la clase Sección. |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Body](../../aspose.words/section/body/) { get; } | Devuelve el[`Body`](../body/) nodo hijo de la sección. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Obtiene el número de hijos inmediatos de este nodo. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Especifica el identificador de nodo personalizado. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Obtiene el documento al que pertenece este nodo. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Obtiene el primer hijo del nodo. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Devoluciones`verdadero` si este nodo tiene nodos secundarios. |
| [HeadersFooters](../../aspose.words/section/headersfooters/) { get; } | Proporciona acceso a los nodos de encabezados y pies de página de la sección. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Devoluciones`verdadero` ya que este nodo puede tener nodos secundarios. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Obtiene el último hijo del nodo. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Obtiene el nodo que sigue inmediatamente a este nodo. |
| override [NodeType](../../aspose.words/section/nodetype/) { get; } | DevolucionesSection . |
| [PageSetup](../../aspose.words/section/pagesetup/) { get; } | Devuelve un objeto que representa la configuración de página y las propiedades de sección. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Obtiene el padre inmediato de este nodo. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Obtiene el nodo inmediatamente anterior a este nodo. |
| [ProtectedForForms](../../aspose.words/section/protectedforforms/) { get; set; } | Verdadero si la sección está protegida para formularios. Cuando una sección está protegida para formularios, los usuarios pueden seleccionar y modificar texto solo en los campos de formulario en Microsoft Word. |
| [Range](../../aspose.words/node/range/) { get; } | Devuelve un[`Range`](../range/) objeto que representa la parte de un documento contenido en este nodo. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| override [Accept](../../aspose.words/section/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Acepta un visitante. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(*[Node](../node/)*) | Agrega el nodo especificado al final de la lista de nodos secundarios para este nodo. |
| [AppendContent](../../aspose.words/section/appendcontent/)(*Section*) | Inserta una copia del contenido de la sección fuente al final de esta sección. |
| [ClearContent](../../aspose.words/section/clearcontent/)() | Borra la sección. |
| [ClearHeadersFooters](../../aspose.words/section/clearheadersfooters/)() | Borra los encabezados y pies de página de esta sección. |
| [Clone](../../aspose.words/section/clone/#clone_1)() | Crea un duplicado de esta sección. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Crea un duplicado del nodo. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Crea un navegador que se puede utilizar para atravesar y leer nodos. |
| [DeleteHeaderFooterShapes](../../aspose.words/section/deleteheaderfootershapes/)() | Elimina todas las formas (objetos de dibujo) de los encabezados y pies de página de esta sección. |
| [EnsureMinimum](../../aspose.words/section/ensureminimum/)() | Asegura que la sección tiene[`Body`](./body/) con uno[`Paragraph`](../paragraph/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | Obtiene el primer ancestro del especificado[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Obtiene el primer antepasado del tipo de objeto especificado. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../nodetype/), int, bool*) | Devuelve un enésimo nodo secundario que coincide con el tipo especificado. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../nodetype/), bool*) | Devuelve una colección activa de nodos secundarios que coinciden con el tipo especificado. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Proporciona soporte para cada iteración de estilo sobre los nodos secundarios de este nodo. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Obtiene el texto de este nodo y de todos sus hijos. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../node/)*) | Devuelve el índice del nodo secundario especificado en la matriz de nodos secundarios. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(*[Node](../node/), [Node](../node/)*) | Inserta el nodo especificado inmediatamente después del nodo de referencia especificado. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(*[Node](../node/), [Node](../node/)*) | Inserta el nodo especificado inmediatamente antes del nodo de referencia especificado. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../node/)*) | Obtiene el siguiente nodo según el algoritmo transversal del árbol de pedidos anticipados. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(*[Node](../node/)*) | Agrega el nodo especificado al principio de la lista de nodos secundarios para este nodo. |
| [PrependContent](../../aspose.words/section/prependcontent/)(*Section*) | Inserta una copia del contenido de la sección fuente al principio de esta sección. |
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

`Section` puede tener uno[`Body`](../body/) y máximo uno[`HeaderFooter`](../headerfooter/) de cada uno[`HeaderFooterType`](../headerfootertype/) .[`Body`](../body/) y[`HeaderFooter`](../headerfooter/) nodes puede estar en cualquier orden dentro`Section`.

Una sección mínima válida debe tener[`Body`](../body/) con uno[`Paragraph`](../paragraph/).

Cada sección tiene su propio conjunto de propiedades que especifican el tamaño de la página, la orientación, los márgenes, etc.

Puede crear una copia de una sección usando[`Clone`](../node/clone/). La copia se puede insertar en el mismo documento o uno diferente.

Para agregar, insertar o eliminar una sección completa, incluido el salto de sección y las propiedades de la sección , utilice los métodos de[`Sections`](../document/sections/) objeto.

Para copiar e insertar solo el contenido de la sección excluyendo la sección break y las propiedades de la sección, use[`AppendContent`](./appendcontent/) y[`PrependContent`](./prependcontent/) métodos.

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
