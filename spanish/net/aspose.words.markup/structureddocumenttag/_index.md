---
title: Class StructuredDocumentTag
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Markup.StructuredDocumentTag clase. Representa una etiqueta de documento estructurado SDT o control de contenido en un documento.
type: docs
weight: 4060
url: /es/net/aspose.words.markup/structureddocumenttag/
---
## StructuredDocumentTag class

Representa una etiqueta de documento estructurado (SDT o control de contenido) en un documento.

Para obtener más información, visite el[Etiquetas de documentos estructurados o control de contenido](https://docs.aspose.com/words/net/working-with-content-control-sdt/) artículo de documentación.

```csharp
public class StructuredDocumentTag : CompositeNode, IStructuredDocumentTag
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [StructuredDocumentTag](structureddocumenttag/)(DocumentBase, SdtType, MarkupLevel) | Inicializa una nueva instancia del **Etiqueta de documento estructurado** clase. |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Appearance](../../aspose.words.markup/structureddocumenttag/appearance/) { get; set; } | Obtiene/establece la apariencia de una etiqueta de documento estructurado. |
| [BuildingBlockCategory](../../aspose.words.markup/structureddocumenttag/buildingblockcategory/) { get; set; } | Especifica la categoría del bloque de creación para este **TED** node. No puede ser`nulo` . |
| [BuildingBlockGallery](../../aspose.words.markup/structureddocumenttag/buildingblockgallery/) { get; set; } | Especifica el tipo de bloque de creación para este **TED** . No puede ser`nulo` . |
| [CalendarType](../../aspose.words.markup/structureddocumenttag/calendartype/) { get; set; } | Especifica el tipo de calendario para este **TED** . El valor predeterminado esDefault |
| [Checked](../../aspose.words.markup/structureddocumenttag/checked/) { get; set; } | Obtiene/establece el estado actual de la casilla de verificación **TED** . El valor predeterminado para esta propiedad es`FALSO` . |
| [Color](../../aspose.words.markup/structureddocumenttag/color/) { get; set; } | Obtiene o establece el color de la etiqueta del documento estructurado. |
| [ContentsFont](../../aspose.words.markup/structureddocumenttag/contentsfont/) { get; } | Formato de fuente que se aplicará al texto ingresado **TED** . |
| [Count](../../aspose.words/compositenode/count/) { get; } | Obtiene el número de hijos inmediatos de este nodo. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Especifica el identificador de nodo personalizado. |
| [DateDisplayFormat](../../aspose.words.markup/structureddocumenttag/datedisplayformat/) { get; set; } | Cadena que representa el formato en el que se muestran las fechas. No puede ser`nulo` . Las fechas para inglés (EE. UU.) son "mm/dd/yyyy" |
| [DateDisplayLocale](../../aspose.words.markup/structureddocumenttag/datedisplaylocale/) { get; set; } | Permite configurar/obtener el formato de idioma para la fecha que se muestra en este **TED** . |
| [DateStorageFormat](../../aspose.words.markup/structureddocumenttag/datestorageformat/) { get; set; } | Obtiene/establece el formato en el que se almacena la fecha para una fecha SDT cuando **TED**está vinculado a un nodo XML en el almacén de datos del documento. El valor predeterminado esDateTime |
| virtual [Document](../../aspose.words/node/document/) { get; } | Obtiene el documento al que pertenece este nodo. |
| [EndCharacterFont](../../aspose.words.markup/structureddocumenttag/endcharacterfont/) { get; } | Formato de fuente que se aplicará al último carácter del texto ingresado **TED** . |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Obtiene el primer hijo del nodo. |
| [FullDate](../../aspose.words.markup/structureddocumenttag/fulldate/) { get; set; } | Especifica la fecha y hora completas ingresadas por última vez en este **TED** . |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Devoluciones`verdadero` si este nodo tiene nodos secundarios. |
| [Id](../../aspose.words.markup/structureddocumenttag/id/) { get; } | Especifica una identificación numérica persistente única de solo lectura para esto **TED**. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Devoluciones`verdadero` ya que este nodo puede tener nodos secundarios. |
| [IsShowingPlaceholderText](../../aspose.words.markup/structureddocumenttag/isshowingplaceholdertext/) { get; set; } | Especifica si el contenido de este **TED**se interpretará como que contiene texto de marcador de posición (a diferencia del contenido de texto normal dentro del SDT). |
| [IsTemporary](../../aspose.words.markup/structureddocumenttag/istemporary/) { get; set; } | Especifica si esto **TED** se eliminará del documento WordProcessingML cuando se modifique su contenido . |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Obtiene el último hijo del nodo. |
| [Level](../../aspose.words.markup/structureddocumenttag/level/) { get; } | Obtiene el nivel en el que este **TED** ocurre en el árbol del documento. |
| [ListItems](../../aspose.words.markup/structureddocumenttag/listitems/) { get; } | Obtiene[`SdtListItemCollection`](../sdtlistitemcollection/) asociado con esto **TED** . |
| [LockContentControl](../../aspose.words.markup/structureddocumenttag/lockcontentcontrol/) { get; set; } | Cuando se establece en`verdadero` , esta propiedad prohibirá a un usuario eliminar esto **TED** . |
| [LockContents](../../aspose.words.markup/structureddocumenttag/lockcontents/) { get; set; } | Cuando se establece en`verdadero` , esta propiedad prohibirá a un usuario editar el contenido de este **TED** . |
| [Multiline](../../aspose.words.markup/structureddocumenttag/multiline/) { get; set; } | Especifica si esto **TED** permite múltiples líneas de texto. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Obtiene el nodo que sigue inmediatamente a este nodo. |
| override [NodeType](../../aspose.words.markup/structureddocumenttag/nodetype/) { get; } | DevolucionesStructuredDocumentTag . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Obtiene el padre inmediato de este nodo. |
| [Placeholder](../../aspose.words.markup/structureddocumenttag/placeholder/) { get; } | Obtiene el[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/)que contiene texto de marcador de posición que debe mostrarse cuando el contenido de esta ejecución de SDT está vacío, el elemento XML asignado asociado está vacío como se especifica mediante el[`XmlMapping`](./xmlmapping/) element o el[`IsShowingPlaceholderText`](./isshowingplaceholdertext/) elemento es`verdadero` . |
| [PlaceholderName](../../aspose.words.markup/structureddocumenttag/placeholdername/) { get; set; } | Obtiene o establece el nombre del[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/) que contiene texto de marcador de posición. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Obtiene el nodo inmediatamente anterior a este nodo. |
| [Range](../../aspose.words/node/range/) { get; } | Devuelve un[`Range`](../../aspose.words/range/) objeto que representa la parte de un documento contenido en este nodo. |
| [SdtType](../../aspose.words.markup/structureddocumenttag/sdttype/) { get; } | Obtiene el tipo de esto **Etiqueta de documento estructurado** . |
| [Style](../../aspose.words.markup/structureddocumenttag/style/) { get; set; } | Obtiene o establece el estilo de la etiqueta del documento estructurado. |
| [StyleName](../../aspose.words.markup/structureddocumenttag/stylename/) { get; set; } | Obtiene o establece el nombre del estilo aplicado a la etiqueta del documento estructurado. |
| [Tag](../../aspose.words.markup/structureddocumenttag/tag/) { get; set; } | Especifica una etiqueta asociada con el nodo SDT actual. No se puede`nulo` . |
| [Title](../../aspose.words.markup/structureddocumenttag/title/) { get; set; } | Especifica el nombre descriptivo asociado con este **TED** . No puede ser`nulo` . |
| [WordOpenXML](../../aspose.words.markup/structureddocumenttag/wordopenxml/) { get; } | Obtiene una cadena que representa el XML contenido dentro del nodo en elFlatOpc formato. |
| [WordOpenXMLMinimal](../../aspose.words.markup/structureddocumenttag/wordopenxmlminimal/) { get; } | Obtiene una cadena que representa el XML contenido dentro del nodo en elFlatOpc format. A diferencia del[`WordOpenXML`](./wordopenxml/)propiedad, este método genera un documento simplificado que excluye cualquier parte no relacionada con el contenido. |
| [XmlMapping](../../aspose.words.markup/structureddocumenttag/xmlmapping/) { get; } | Obtiene un objeto que representa la asignación de esta etiqueta de documento estructurado a datos XML en una parte XML personalizada del documento actual. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| override [Accept](../../aspose.words.markup/structureddocumenttag/accept/)(DocumentVisitor) | Acepta un visitante. |
| override [AcceptEnd](../../aspose.words.markup/structureddocumenttag/acceptend/)(DocumentVisitor) |  |
| override [AcceptStart](../../aspose.words.markup/structureddocumenttag/acceptstart/)(DocumentVisitor) |  |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(T) |  |
| [Clear](../../aspose.words.markup/structureddocumenttag/clear/)() | Borra el contenido de esta etiqueta de documento estructurado y muestra un marcador de posición si está definido. |
| [Clone](../../aspose.words/node/clone/)(bool) | Crea un duplicado del nodo. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Crea un navegador que se puede utilizar para atravesar y leer nodos. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Obtiene el primer ancestro del especificado[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Obtiene el primer antepasado del tipo de objeto especificado. |
| [GetChild](../../aspose.words/compositenode/getchild/)(NodeType, int, bool) | Devuelve un enésimo nodo secundario que coincide con el tipo especificado. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(NodeType, bool) | Devuelve una colección activa de nodos secundarios que coinciden con el tipo especificado. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Proporciona soporte para cada iteración de estilo sobre los nodos secundarios de este nodo. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Obtiene el texto de este nodo y de todos sus hijos. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(Node) | Devuelve el índice del nodo secundario especificado en la matriz de nodos secundarios. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(T, Node) |  |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(T, Node) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Obtiene el siguiente nodo según el algoritmo transversal del árbol de pedidos anticipados. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Obtiene el nodo anterior según el algoritmo transversal del árbol de pedidos anticipados. |
| [Remove](../../aspose.words/node/remove/)() | Se elimina del padre. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Elimina todos los nodos secundarios del nodo actual. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(T) |  |
| [RemoveSelfOnly](../../aspose.words.markup/structureddocumenttag/removeselfonly/)() | Elimina solo este nodo SDT, pero mantiene su contenido dentro del árbol de documentos. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Elimina todo[`SmartTag`](../smarttag/)nodos descendientes del nodo actual. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(string) | Selecciona una lista de nodos que coinciden con la expresión XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | Selecciona el primero[`Node`](../../aspose.words/node/) que coincide con la expresión XPath. |
| [SetCheckedSymbol](../../aspose.words.markup/structureddocumenttag/setcheckedsymbol/)(int, string) | Establece el símbolo utilizado para representar el estado marcado de un control de contenido de casilla de verificación. |
| [SetUncheckedSymbol](../../aspose.words.markup/structureddocumenttag/setuncheckedsymbol/)(int, string) | Establece el símbolo utilizado para representar el estado no marcado de un control de contenido de casilla de verificación. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Exporta el contenido del nodo a una cadena en el formato especificado. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Exporta el contenido del nodo a una cadena usando las opciones de guardado especificadas. |

### Observaciones

Las etiquetas de documentos estructurados (SDT) permiten incorporar semántica definida por el cliente, así como su comportamiento y apariencia en un documento.

En esta versión, Aspose.Words proporciona una serie de métodos y propiedades públicos para manipular el comportamiento y el contenido de`StructuredDocumentTag` . La asignación de nodos SDT a paquetes XML personalizados dentro de un documento se puede realizar usando el[`XmlMapping`](./xmlmapping/) propiedad.

`StructuredDocumentTag` puede aparecer en un documento en los siguientes lugares:

* Nivel de bloque: entre párrafos y tablas, como hijo de un[`Body`](../../aspose.words/body/) ,[`HeaderFooter`](../../aspose.words/headerfooter/) , [`Comment`](../../aspose.words/comment/) ,[`Footnote`](../../aspose.words.notes/footnote/) o un[`Shape`](../../aspose.words.drawing/shape/) nodo.
* Nivel de fila: entre filas de una tabla, como elemento secundario de una[`Table`](../../aspose.words.tables/table/) nodo.
* Nivel de celda: entre celdas de una fila de la tabla, como elemento secundario de un[`Row`](../../aspose.words.tables/row/) nodo.
* Nivel en línea: entre el contenido en línea interno, como hijo de un[`Paragraph`](../../aspose.words/paragraph/).
* Anidado dentro de otro`StructuredDocumentTag`.

### Ejemplos

Muestra cómo trabajar con estilos para elementos de control de contenido.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// A continuación se muestran dos formas de aplicar un estilo del documento a una etiqueta de documento estructurado.
// 1 - Aplicar un objeto de estilo de la colección de estilos del documento:
Style quoteStyle = doc.Styles[StyleIdentifier.Quote];
StructuredDocumentTag sdtPlainText =
    new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline) { Style = quoteStyle };

// 2 - Referencia a un estilo en el documento por nombre:
StructuredDocumentTag sdtRichText =
    new StructuredDocumentTag(doc, SdtType.RichText, MarkupLevel.Inline) { StyleName = "Quote" };

builder.InsertNode(sdtPlainText);
builder.InsertNode(sdtRichText);

Assert.AreEqual(NodeType.StructuredDocumentTag, sdtPlainText.NodeType);

NodeCollection tags = doc.GetChildNodes(NodeType.StructuredDocumentTag, true);

foreach (Node node in tags)
{
    StructuredDocumentTag sdt = (StructuredDocumentTag)node;

    Console.WriteLine(sdt.WordOpenXMLMinimal);

    Assert.AreEqual(StyleIdentifier.Quote, sdt.Style.StyleIdentifier);
    Assert.AreEqual("Quote", sdt.StyleName);
}
```

### Ver también

* class [CompositeNode](../../aspose.words/compositenode/)
* interface [IStructuredDocumentTag](../istructureddocumenttag/)
* espacio de nombres [Aspose.Words.Markup](../../aspose.words.markup/)
* asamblea [Aspose.Words](../../)


