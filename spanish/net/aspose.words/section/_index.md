---
title: Section
second_title: Referencia de API de Aspose.Words para .NET
description: Representa una sola sección en un documento.
type: docs
weight: 5440
url: /es/net/aspose.words/section/
---
## Section class

Representa una sola sección en un documento.

```csharp
public sealed class Section : CompositeNode
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [Section](section/)(DocumentBase) | Inicializa una nueva instancia de la clase Sección. |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Body](../../aspose.words/section/body/) { get; } | Devuelve el **Cuerpo** nodo hijo de la sección. |
| [ChildNodes](../../aspose.words/compositenode/childnodes/) { get; } | Obtiene todos los nodos secundarios inmediatos de este nodo. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Obtiene el número de hijos inmediatos de este nodo. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Especifica el identificador de nodo personalizado. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Obtiene el documento al que pertenece este nodo. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Obtiene el primer hijo del nodo. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Devuelve verdadero si este nodo tiene nodos secundarios. |
| [HeadersFooters](../../aspose.words/section/headersfooters/) { get; } | Proporciona acceso a los nodos de encabezados y pies de página de la sección. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Devuelve verdadero ya que este nodo puede tener nodos secundarios. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Obtiene el último hijo del nodo. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Obtiene el nodo que sigue inmediatamente a este nodo. |
| override [NodeType](../../aspose.words/section/nodetype/) { get; } | Devoluciones **NodeType.Sección** . |
| [PageSetup](../../aspose.words/section/pagesetup/) { get; } | Devuelve un objeto que representa la configuración de la página y las propiedades de la sección. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Obtiene el padre inmediato de este nodo. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Obtiene el nodo inmediatamente anterior a este nodo. |
| [ProtectedForForms](../../aspose.words/section/protectedforforms/) { get; set; } | Verdadero si la sección está protegida para formularios. Cuando una sección está protegida para formularios, los usuarios pueden seleccionar y modificar texto solo en campos de formulario en Microsoft Word. |
| [Range](../../aspose.words/node/range/) { get; } | Devuelve un **Rango** objeto que representa la parte de un documento que está contenido en este nodo. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| override [Accept](../../aspose.words/section/accept/)(DocumentVisitor) | Acepta un visitante. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(Node) | Agrega el nodo especificado al final de la lista de nodos secundarios para este nodo. |
| [AppendContent](../../aspose.words/section/appendcontent/)(Section) | Inserta una copia del contenido de la sección fuente al final de esta sección. |
| [ClearContent](../../aspose.words/section/clearcontent/)() | Borra la sección. |
| [ClearHeadersFooters](../../aspose.words/section/clearheadersfooters/)() | Borra los encabezados y pies de página de esta sección. |
| [Clone](../../aspose.words/section/clone/#clone_1)() | Crea un duplicado de esta sección. |
| [Clone](../../aspose.words/node/clone/)(bool) | Crea un duplicado del nodo. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Reservado para uso del sistema. IXPathNavigable. |
| [DeleteHeaderFooterShapes](../../aspose.words/section/deleteheaderfootershapes/)() | Elimina todas las formas (objetos de dibujo) de los encabezados y pies de página de esta sección. |
| [EnsureMinimum](../../aspose.words/section/ensureminimum/)() | Asegura que la sección tenga Cuerpo con un Párrafo. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Obtiene el primer ancestro del especificado[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Obtiene el primer ancestro del tipo de objeto especificado. |
| [GetChild](../../aspose.words/compositenode/getchild/)(NodeType, int, bool) | Devuelve un enésimo nodo secundario que coincide con el tipo especificado. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(NodeType, bool) | Devuelve una colección activa de nodos secundarios que coinciden con el tipo especificado. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Proporciona soporte para la iteración de cada estilo sobre los nodos secundarios de este nodo. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Obtiene el texto de este nodo y de todos sus hijos. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(Node) | Devuelve el índice del nodo secundario especificado en la matriz de nodos secundarios. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(Node, Node) | Inserta el nodo especificado inmediatamente después del nodo de referencia especificado. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(Node, Node) | Inserta el nodo especificado inmediatamente antes del nodo de referencia especificado. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Obtiene el siguiente nodo de acuerdo con el algoritmo de recorrido del árbol de pedido previo. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(Node) | Agrega el nodo especificado al principio de la lista de nodos secundarios para este nodo. |
| [PrependContent](../../aspose.words/section/prependcontent/)(Section) | Inserta una copia del contenido de la sección fuente al principio de esta sección. |
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

**Sección** puede tener uno[`Body`](./body/) y maximo uno[`HeaderFooter`](../headerfooter/) de cada[`HeaderFooterType`](../headerfootertype/) . **Cuerpo** y **EncabezadoPie de página** nodes puede estar en cualquier orden dentro **Sección**.

Una sección válida mínima debe tener **Cuerpo** con uno **Párrafo**.

Cada sección tiene su propio conjunto de propiedades que especifican el tamaño de la página, la orientación, los márgenes, etc.

Puede crear una copia de una sección usando[`Clone`](../node/clone/). La copia se puede insertar en el mismo documento o uno diferente.

Para agregar, insertar o eliminar una sección completa, incluidos los saltos de sección y las propiedades de la sección , utilice los métodos de la **Secciones** objeto.

Para copiar e insertar solo el contenido de la sección, excluyendo la sección break y las propiedades de la sección, use **Agregar contenido** y **AnteponerContenido**métodos.

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
