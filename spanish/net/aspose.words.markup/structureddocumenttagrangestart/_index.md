---
title: StructuredDocumentTagRangeStart
second_title: Referencia de API de Aspose.Words para .NET
description: Representa un inicio de a distancia etiqueta de documento estructurado que acepta contenido de varias secciones. Véase tambiénStructuredDocumentTagRangeEnd./structureddocumenttagrangeend .
type: docs
weight: 3850
url: /es/net/aspose.words.markup/structureddocumenttagrangestart/
---
## StructuredDocumentTagRangeStart class

Representa un inicio de **a distancia** etiqueta de documento estructurado que acepta contenido de varias secciones. Véase también[`StructuredDocumentTagRangeEnd`](../structureddocumenttagrangeend) .

```csharp
public class StructuredDocumentTagRangeStart : Node, IEnumerable<Node>, IStructuredDocumentTag
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [StructuredDocumentTagRangeStart](structureddocumenttagrangestart)(DocumentBase, SdtType) | Inicializa una nueva instancia del **Comienzo del rango de etiquetas de documentos estructurados** clase. |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [ChildNodes](../../aspose.words.markup/structureddocumenttagrangestart/childnodes) { get; } | Obtiene todos los nodos entre este nodo inicial de rango y el nodo final de rango. |
| [Color](../../aspose.words.markup/structureddocumenttagrangestart/color) { get; set; } | Obtiene o establece el color de la etiqueta del documento estructurado. |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | Especifica el identificador de nodo personalizado. |
| virtual [Document](../../aspose.words/node/document) { get; } | Obtiene el documento al que pertenece este nodo. |
| [Id](../../aspose.words.markup/structureddocumenttagrangestart/id) { get; } | Especifica un Id. numérico persistente único de solo lectura para esta etiqueta de documento estructurado. |
| virtual [IsComposite](../../aspose.words/node/iscomposite) { get; } | Devuelve verdadero si este nodo puede contener otros nodos. |
| [IsShowingPlaceholderText](../../aspose.words.markup/structureddocumenttagrangestart/isshowingplaceholdertext) { get; set; } | Especifica si se interpretará que el contenido de esta etiqueta de documento estructurado contiene texto de marcador de posición (a diferencia del contenido de texto normal dentro de la etiqueta de documento estructurado). |
| [LastChild](../../aspose.words.markup/structureddocumenttagrangestart/lastchild) { get; } | Obtiene el último hijo en el rango stdContent. |
| [Level](../../aspose.words.markup/structureddocumenttagrangestart/level) { get; } | Obtiene el nivel en el que se produce este inicio de rango de etiqueta de documento estructurado en el árbol del documento. |
| [LockContentControl](../../aspose.words.markup/structureddocumenttagrangestart/lockcontentcontrol) { get; set; } | Cuando se establece en verdadero, esta propiedad prohibirá que un usuario elimine esta etiqueta de documento estructurado. |
| [LockContents](../../aspose.words.markup/structureddocumenttagrangestart/lockcontents) { get; set; } | Cuando se establece en verdadero, esta propiedad prohibirá que un usuario edite el contenido de esta etiqueta de documento estructurado. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | Obtiene el nodo que sigue inmediatamente a este nodo. |
| override [NodeType](../../aspose.words.markup/structureddocumenttagrangestart/nodetype) { get; } |  |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | Obtiene el padre inmediato de este nodo. |
| [Placeholder](../../aspose.words.markup/structureddocumenttagrangestart/placeholder) { get; } | Obtiene el[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock) que contiene texto de marcador de posición que debe mostrarse cuando el contenido de ejecución de esta etiqueta de documento estructurado está vacío, el elemento XML asignado asociado está vacío como se especifica a través del[`XmlMapping`](./xmlmapping) elemento o el[`IsShowingPlaceholderText`](./isshowingplaceholdertext) elemento es verdadero. |
| [PlaceholderName](../../aspose.words.markup/structureddocumenttagrangestart/placeholdername) { get; set; } | Obtiene o establece el Nombre del[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock) que contiene texto de marcador de posición. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | Obtiene el nodo inmediatamente anterior a este nodo. |
| [Range](../../aspose.words/node/range) { get; } | Devuelve un **Rango** objeto que representa la parte de un documento que está contenido en este nodo. |
| [RangeEnd](../../aspose.words.markup/structureddocumenttagrangestart/rangeend) { get; } | Especifica el final del rango si StructuredDocumentTag es una etiqueta de documento estructurado de rango. De lo contrario devuelve nulo. |
| [SdtType](../../aspose.words.markup/structureddocumenttagrangestart/sdttype) { get; } | Obtiene el tipo de esta etiqueta de documento estructurado. |
| [Tag](../../aspose.words.markup/structureddocumenttagrangestart/tag) { get; set; } | Especifica una etiqueta asociada con el nodo de etiqueta del documento estructurado actual. No puede ser nulo. |
| [Title](../../aspose.words.markup/structureddocumenttagrangestart/title) { get; set; } | Especifica el nombre descriptivo asociado con esta etiqueta de documento estructurado. No puede ser nulo. |
| [WordOpenXML](../../aspose.words.markup/structureddocumenttagrangestart/wordopenxml) { get; } | Obtiene una cadena que representa el XML contenido dentro del nodo en elFlatOpc formato. |
| [XmlMapping](../../aspose.words.markup/structureddocumenttagrangestart/xmlmapping) { get; } | Obtiene un objeto que representa la asignación de este rango de etiquetas de documento estructurado a datos XML en una parte XML personalizada del documento actual. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| override [Accept](../../aspose.words.markup/structureddocumenttagrangestart/accept)(DocumentVisitor) |  |
| [AppendChild](../../aspose.words.markup/structureddocumenttagrangestart/appendchild)(Node) | Agrega el nodo especificado al final del rango de stdContent. |
| [Clone](../../aspose.words/node/clone)(bool) | Crea un duplicado del nodo. |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | Obtiene el primer ancestro del especificado[`NodeType`](../../aspose.words/nodetype) . |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | Obtiene el primer ancestro del tipo de objeto especificado. |
| [GetChildNodes](../../aspose.words.markup/structureddocumenttagrangestart/getchildnodes)(NodeType, bool) | Devuelve una colección activa de nodos secundarios que coinciden con los tipos especificados. |
| [GetEnumerator](../../aspose.words.markup/structureddocumenttagrangestart/getenumerator)() | Proporciona soporte para la iteración de cada estilo sobre los nodos secundarios de este nodo. |
| virtual [GetText](../../aspose.words/node/gettext)() | Obtiene el texto de este nodo y de todos sus hijos. |
| [NextPreOrder](../../aspose.words/node/nextpreorder)(Node) | Obtiene el siguiente nodo de acuerdo con el algoritmo de recorrido del árbol de pedido previo. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder)(Node) | Obtiene el nodo anterior de acuerdo con el algoritmo de recorrido del árbol de pedido previo. |
| [Remove](../../aspose.words/node/remove)() | Se elimina a sí mismo del padre. |
| [RemoveAllChildren](../../aspose.words.markup/structureddocumenttagrangestart/removeallchildren)() | Elimina todos los nodos entre este nodo inicial de rango y el nodo final de rango. |
| [RemoveSelfOnly](../../aspose.words.markup/structureddocumenttagrangestart/removeselfonly)() | Elimina este inicio de rango y los nodos finales de rango apropiados de la etiqueta del documento estructurado, pero mantiene su contenido dentro del árbol del documento. |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | Exporta el contenido del nodo a una cadena en el formato especificado. |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | Exporta el contenido del nodo a una cadena utilizando las opciones de guardado especificadas. |

### Observaciones

Puede ser hijo inmediato de[`Body`](../../aspose.words/body) nodo **solamente** .

### Ejemplos

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

* class [Node](../../aspose.words/node)
* interface [IStructuredDocumentTag](../istructureddocumenttag)
* espacio de nombres [Aspose.Words.Markup](../../aspose.words.markup)
* asamblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
