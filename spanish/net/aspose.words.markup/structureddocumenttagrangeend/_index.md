---
title: Class StructuredDocumentTagRangeEnd
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Markup.StructuredDocumentTagRangeEnd clase. Representa el final de a distancia etiqueta de documento estructurado que acepta contenido de varias secciones. Véase tambiénStructuredDocumentTagRangeStart nodo.
type: docs
weight: 4080
url: /es/net/aspose.words.markup/structureddocumenttagrangeend/
---
## StructuredDocumentTagRangeEnd class

Representa el final de **a distancia** etiqueta de documento estructurado que acepta contenido de varias secciones. Véase también[`StructuredDocumentTagRangeStart`](../structureddocumenttagrangestart/) nodo.

Para obtener más información, visite el[Etiquetas de documentos estructurados o control de contenido](https://docs.aspose.com/words/net/working-with-content-control-sdt/) artículo de documentación.

```csharp
public class StructuredDocumentTagRangeEnd : Node
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [StructuredDocumentTagRangeEnd](structureddocumenttagrangeend/)(DocumentBase, int) | Inicializa una nueva instancia del **Fin del rango de etiquetas de documentos estructurados** clase. |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Especifica el identificador de nodo personalizado. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Obtiene el documento al que pertenece este nodo. |
| [Id](../../aspose.words.markup/structureddocumenttagrangeend/id/) { get; } | Especifica una identificación numérica persistente única de solo lectura para este **Rango de etiquetas de documentos estructurados** nodo. Correspondiente[`StructuredDocumentTagRangeStart`](../structureddocumenttagrangestart/) el nodo tiene el mismo[`Id`](../structureddocumenttagrangestart/id/) . |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | Devoluciones`verdadero` si este nodo puede contener otros nodos. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Obtiene el nodo que sigue inmediatamente a este nodo. |
| override [NodeType](../../aspose.words.markup/structureddocumenttagrangeend/nodetype/) { get; } | DevolucionesStructuredDocumentTagRangeEnd . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Obtiene el padre inmediato de este nodo. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Obtiene el nodo inmediatamente anterior a este nodo. |
| [Range](../../aspose.words/node/range/) { get; } | Devuelve un[`Range`](../../aspose.words/range/) objeto que representa la parte de un documento contenido en este nodo. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| override [Accept](../../aspose.words.markup/structureddocumenttagrangeend/accept/)(DocumentVisitor) | Acepta un visitante. |
| [Clone](../../aspose.words/node/clone/)(bool) | Crea un duplicado del nodo. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Obtiene el primer ancestro del especificado[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Obtiene el primer antepasado del tipo de objeto especificado. |
| virtual [GetText](../../aspose.words/node/gettext/)() | Obtiene el texto de este nodo y de todos sus hijos. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Obtiene el siguiente nodo según el algoritmo transversal del árbol de pedidos anticipados. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Obtiene el nodo anterior según el algoritmo transversal del árbol de pedidos anticipados. |
| [Remove](../../aspose.words/node/remove/)() | Se elimina del padre. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Exporta el contenido del nodo a una cadena en el formato especificado. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Exporta el contenido del nodo a una cadena usando las opciones de guardado especificadas. |

### Observaciones

Puede ser hijo inmediato de[`Body`](../../aspose.words/body/) nodo **solo** .

### Ejemplos

Muestra cómo obtener las propiedades de etiquetas de documentos estructurados de varias secciones.

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
* espacio de nombres [Aspose.Words.Markup](../../aspose.words.markup/)
* asamblea [Aspose.Words](../../)


