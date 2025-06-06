---
title: StructuredDocumentTagRangeStart Class
linktitle: StructuredDocumentTagRangeStart
articleTitle: StructuredDocumentTagRangeStart
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Markup.StructuredDocumentTagRangeStart, que permite una gestión fluida de contenido de múltiples secciones en documentos estructurados.
type: docs
weight: 4780
url: /es/net/aspose.words.markup/structureddocumenttagrangestart/
---
## StructuredDocumentTagRangeStart class

Representa un inicio de**a distancia** Etiqueta de documento estructurado que acepta contenido de varias secciones. Véase también[`StructuredDocumentTagRangeEnd`](../structureddocumenttagrangeend/) .

Para obtener más información, visite el[Etiquetas de documentos estructurados o control de contenido](https://docs.aspose.com/words/net/working-with-content-control-sdt/) Artículo de documentación.

```csharp
public class StructuredDocumentTagRangeStart : Node, IEnumerable<Node>, IStructuredDocumentTag
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [StructuredDocumentTagRangeStart](structureddocumenttagrangestart/)(*[DocumentBase](../../aspose.words/documentbase/), [SdtType](../sdttype/)*) | Inicializa una nueva instancia del**Inicio del rango de etiquetas de documentos estructurados** clase. |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Appearance](../../aspose.words.markup/structureddocumenttagrangestart/appearance/) { get; set; } | Obtiene o establece la apariencia de la etiqueta del documento estructurado. |
| [Color](../../aspose.words.markup/structureddocumenttagrangestart/color/) { get; set; } | Obtiene o establece el color de la etiqueta del documento estructurado. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Especifica un identificador de nodo personalizado. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Obtiene el documento al que pertenece este nodo. |
| [Id](../../aspose.words.markup/structureddocumenttagrangestart/id/) { get; } | Especifica un identificador numérico persistente único de solo lectura para esta etiqueta de documento estructurado. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | Devuelve`verdadero` si este nodo puede contener otros nodos. |
| [IsShowingPlaceholderText](../../aspose.words.markup/structureddocumenttagrangestart/isshowingplaceholdertext/) { get; set; } | Especifica si el contenido de esta etiqueta de documento estructurado se debe interpretar como que contiene texto de marcador de posición (a diferencia del contenido de texto normal dentro de la etiqueta de documento estructurado). |
| [LastChild](../../aspose.words.markup/structureddocumenttagrangestart/lastchild/) { get; } | Obtiene el último hijo en el rango stdContent. |
| [Level](../../aspose.words.markup/structureddocumenttagrangestart/level/) { get; } | Obtiene el nivel en el que se produce el inicio del rango de etiquetas de este documento estructurado en el árbol del documento. |
| [LockContentControl](../../aspose.words.markup/structureddocumenttagrangestart/lockcontentcontrol/) { get; set; } | Cuando se establece en`verdadero` , esta propiedad prohibirá que un usuario elimine esta etiqueta de documento estructurado. |
| [LockContents](../../aspose.words.markup/structureddocumenttagrangestart/lockcontents/) { get; set; } | Cuando se establece en`verdadero` , esta propiedad prohibirá que un usuario edite el contenido de esta etiqueta de documento estructurado. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Obtiene el nodo inmediatamente siguiente a este nodo. |
| override [NodeType](../../aspose.words.markup/structureddocumenttagrangestart/nodetype/) { get; } | DevuelveStructuredDocumentTagRangeStart . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Obtiene el padre inmediato de este nodo. |
| [Placeholder](../../aspose.words.markup/structureddocumenttagrangestart/placeholder/) { get; } | Obtiene el[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/)que contiene texto de marcador de posición que debe mostrarse cuando este contenido de ejecución de etiqueta de documento estructurado está vacío, el elemento XML mapeado asociado está vacío como se especifica a través de[`XmlMapping`](./xmlmapping/) elemento o el[`IsShowingPlaceholderText`](./isshowingplaceholdertext/) elemento es`verdadero` . |
| [PlaceholderName](../../aspose.words.markup/structureddocumenttagrangestart/placeholdername/) { get; set; } | Obtiene o establece el nombre del[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/) contiene texto de marcador de posición. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Obtiene el nodo inmediatamente anterior a este nodo. |
| [Range](../../aspose.words/node/range/) { get; } | Devuelve un[`Range`](../../aspose.words/range/)objeto que representa la porción de un documento que está contenida en este nodo. |
| [RangeEnd](../../aspose.words.markup/structureddocumenttagrangestart/rangeend/) { get; } | Especifica el final del rango si el[`StructuredDocumentTag`](../structureddocumenttag/) es una etiqueta de documento estructurada de rango. De lo contrario, devuelve`nulo` . |
| [SdtType](../../aspose.words.markup/structureddocumenttagrangestart/sdttype/) { get; } | Obtiene el tipo de esta etiqueta de documento estructurado. |
| [Tag](../../aspose.words.markup/structureddocumenttagrangestart/tag/) { get; set; } | Especifica una etiqueta asociada con el nodo de etiqueta del documento estructurado actual. No se puede`nulo` . |
| [Title](../../aspose.words.markup/structureddocumenttagrangestart/title/) { get; set; } | Especifica el nombre descriptivo asociado con esta etiqueta de documento estructurado. No se puede`nulo` . |
| [WordOpenXML](../../aspose.words.markup/structureddocumenttagrangestart/wordopenxml/) { get; } | Obtiene una cadena que representa el XML contenido dentro del nodo en elFlatOpc formato. |
| [WordOpenXMLMinimal](../../aspose.words.markup/structureddocumenttagrangestart/wordopenxmlminimal/) { get; } | Obtiene una cadena que representa el XML contenido dentro del nodo en elFlatOpc format. A diferencia del[`WordOpenXML`](./wordopenxml/) propiedad, este método genera un documento simplificado que excluye cualquier parte no relacionada con el contenido. |
| [XmlMapping](../../aspose.words.markup/structureddocumenttagrangestart/xmlmapping/) { get; } | Obtiene un objeto que representa la asignación de este rango de etiquetas de documento estructurado a datos XML en una parte XML personalizada del documento actual. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| override [Accept](../../aspose.words.markup/structureddocumenttagrangestart/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Acepta un visitante. |
| [AppendChild](../../aspose.words.markup/structureddocumenttagrangestart/appendchild/)(*[Node](../../aspose.words/node/)*) | Agrega el nodo especificado al final del rango stdContent. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Crea un duplicado del nodo. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | Obtiene el primer ancestro del especificado[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Obtiene el primer ancestro del tipo de objeto especificado. |
| [GetChildNodes](../../aspose.words.markup/structureddocumenttagrangestart/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | Devuelve una colección activa de nodos secundarios que coinciden con los tipos especificados. |
| [GetEnumerator](../../aspose.words.markup/structureddocumenttagrangestart/getenumerator/)() | Proporciona soporte para cada iteración de estilo sobre los nodos secundarios de este nodo. |
| virtual [GetText](../../aspose.words/node/gettext/)() | Obtiene el texto de este nodo y de todos sus hijos. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | Obtiene el siguiente nodo según el algoritmo de recorrido del árbol de preorden. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | Obtiene el nodo anterior según el algoritmo de recorrido del árbol de preorden. |
| [Remove](../../aspose.words/node/remove/)() | Se elimina a sí mismo del padre. |
| [RemoveAllChildren](../../aspose.words.markup/structureddocumenttagrangestart/removeallchildren/)() | Elimina todos los nodos entre este nodo de inicio de rango y el nodo de fin de rango. |
| [RemoveSelfOnly](../../aspose.words.markup/structureddocumenttagrangestart/removeselfonly/)() | Elimina los nodos de inicio y fin de rango correspondientes de la etiqueta del documento estructurado, pero mantiene su contenido dentro del árbol del documento. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | Exporta el contenido del nodo en una cadena en el formato especificado. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Exporta el contenido del nodo en una cadena utilizando las opciones de guardado especificadas. |

## Observaciones

Puede ser hijo inmediato de[`Body`](../../aspose.words/body/) nodo**solo** .

## Ejemplos

Muestra cómo obtener las propiedades de las etiquetas de documentos estructurados de varias secciones.

```csharp
Document doc = new Document(MyDir + "Multi-section structured document tags.docx");

StructuredDocumentTagRangeStart rangeStartTag =
    doc.GetChildNodes(NodeType.StructuredDocumentTagRangeStart, true)[0] as StructuredDocumentTagRangeStart;
StructuredDocumentTagRangeEnd rangeEndTag =
    doc.GetChildNodes(NodeType.StructuredDocumentTagRangeEnd, true)[0] as StructuredDocumentTagRangeEnd;

Console.WriteLine("StructuredDocumentTagRangeStart values:");
Console.WriteLine($"\t|Id: {rangeStartTag.Id}");
Console.WriteLine($"\t|Title: {rangeStartTag.Title}");
Console.WriteLine($"\t|PlaceholderName: {rangeStartTag.PlaceholderName}");
Console.WriteLine($"\t|IsShowingPlaceholderText: {rangeStartTag.IsShowingPlaceholderText}");
Console.WriteLine($"\t|LockContentControl: {rangeStartTag.LockContentControl}");
Console.WriteLine($"\t|LockContents: {rangeStartTag.LockContents}");
Console.WriteLine($"\t|Level: {rangeStartTag.Level}");
Console.WriteLine($"\t|NodeType: {rangeStartTag.NodeType}");
Console.WriteLine($"\t|RangeEnd: {rangeStartTag.RangeEnd}");
Console.WriteLine($"\t|Color: {rangeStartTag.Color.ToArgb()}");
Console.WriteLine($"\t|SdtType: {rangeStartTag.SdtType}");
Console.WriteLine($"\t|FlatOpcContent: {rangeStartTag.WordOpenXML}");
Console.WriteLine($"\t|Tag: {rangeStartTag.Tag}\n");

Console.WriteLine("StructuredDocumentTagRangeEnd values:");
Console.WriteLine($"\t|Id: {rangeEndTag.Id}");
Console.WriteLine($"\t|NodeType: {rangeEndTag.NodeType}");
```

### Ver también

* class [Node](../../aspose.words/node/)
* interface [IStructuredDocumentTag](../istructureddocumenttag/)
* espacio de nombres [Aspose.Words.Markup](../../aspose.words.markup/)
* asamblea [Aspose.Words](../../)
