---
title: IStructuredDocumentTag Interface
linktitle: IStructuredDocumentTag
articleTitle: IStructuredDocumentTag
second_title: Aspose.Words para .NET
description: ¡Explore la interfaz Aspose.Words.Markup.IStructuredDocumentTag para una gestión eficiente de etiquetas de documentos estructurados y mejore el procesamiento de sus documentos hoy mismo!
type: docs
weight: 4660
url: /es/net/aspose.words.markup/istructureddocumenttag/
---
## IStructuredDocumentTag interface

Interfaz para definir datos comunes para[`StructuredDocumentTag`](../structureddocumenttag/) y[`StructuredDocumentTagRangeStart`](../structureddocumenttagrangestart/) .

```csharp
public interface IStructuredDocumentTag
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Appearance](../../aspose.words.markup/istructureddocumenttag/appearance/) { get; set; } | Obtiene o establece la apariencia de la etiqueta del documento estructurado. |
| [Color](../../aspose.words.markup/istructureddocumenttag/color/) { get; set; } | Obtiene o establece el color de la etiqueta del documento estructurado. |
| [Id](../../aspose.words.markup/istructureddocumenttag/id/) { get; } | Especifica un identificador numérico persistente único de solo lectura para este**TED**. |
| [IsMultiSection](../../aspose.words.markup/istructureddocumenttag/ismultisection/) { get; } | Devuelve verdadero si esta instancia es una etiqueta de documento estructurado de rango (varias secciones). |
| [IsShowingPlaceholderText](../../aspose.words.markup/istructureddocumenttag/isshowingplaceholdertext/) { get; set; } | Especifica si el contenido de este**TED** se interpretará como que contiene texto de marcador de posición (a diferencia del contenido de texto normal dentro del SDT). |
| [Level](../../aspose.words.markup/istructureddocumenttag/level/) { get; } | Obtiene el nivel en el que este**TED** ocurre en el árbol del documento. |
| [LockContentControl](../../aspose.words.markup/istructureddocumenttag/lockcontentcontrol/) { get; set; } | Cuando se establece como verdadero, esta propiedad prohibirá que un usuario elimine esto**TED** . |
| [LockContents](../../aspose.words.markup/istructureddocumenttag/lockcontents/) { get; set; } | Cuando se establece como verdadera, esta propiedad prohibirá que un usuario edite el contenido de esta**TED** . |
| [Node](../../aspose.words.markup/istructureddocumenttag/node/) { get; } | Devuelve el objeto Node que implementa esta interfaz. |
| [Placeholder](../../aspose.words.markup/istructureddocumenttag/placeholder/) { get; } | Obtiene el[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/) que contiene texto de marcador de posición que debe mostrarse cuando el contenido de esta ejecución SDT está vacío, el elemento XML mapeado asociado está vacío como se especifica mediante[`XmlMapping`](./xmlmapping/) elemento o el[`IsShowingPlaceholderText`](./isshowingplaceholdertext/) el elemento es verdadero. |
| [PlaceholderName](../../aspose.words.markup/istructureddocumenttag/placeholdername/) { get; set; } | Obtiene o establece el nombre del[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/) contiene texto de marcador de posición. |
| [SdtType](../../aspose.words.markup/istructureddocumenttag/sdttype/) { get; } | Obtiene el tipo de esto**Etiqueta de documento estructurado** . |
| [Tag](../../aspose.words.markup/istructureddocumenttag/tag/) { get; set; } | Especifica una etiqueta asociada con el nodo SDT actual. No puede ser nulo. |
| [Title](../../aspose.words.markup/istructureddocumenttag/title/) { get; set; } | Especifica el nombre descriptivo asociado con este**TED** . No puede ser nulo. |
| [WordOpenXML](../../aspose.words.markup/istructureddocumenttag/wordopenxml/) { get; } | Obtiene una cadena que representa el XML contenido dentro del nodo en elFlatOpc formato. |
| [XmlMapping](../../aspose.words.markup/istructureddocumenttag/xmlmapping/) { get; } | Obtiene un objeto que representa la asignación de esta etiqueta de documento estructurado a datos XML en una parte XML personalizada del documento actual. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [GetChildNodes](../../aspose.words.markup/istructureddocumenttag/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | Devuelve una colección activa de nodos secundarios que coinciden con los tipos especificados. |
| [RemoveSelfOnly](../../aspose.words.markup/istructureddocumenttag/removeselfonly/)() | Elimina únicamente este nodo SDT, pero conserva su contenido dentro del árbol del documento. |

## Ejemplos

Muestra cómo eliminar la etiqueta de documento estructurado, pero mantiene el contenido dentro.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");

 // Esta colección proporciona una interfaz unificada para acceder a etiquetas estructuradas con y sin rango.
IEnumerable<IStructuredDocumentTag> sdts = doc.Range.StructuredDocumentTags.ToList();
Assert.AreEqual(5, sdts.Count());

// Aquí podemos obtener nodos secundarios de la interfaz común de etiquetas estructuradas con rango y sin rango.
foreach (IStructuredDocumentTag sdt in sdts)
    if (sdt.GetChildNodes(NodeType.Any, false).Count > 0)
        sdt.RemoveSelfOnly();

sdts = doc.Range.StructuredDocumentTags.ToList();
Assert.AreEqual(0, sdts.Count());
```

### Ver también

* espacio de nombres [Aspose.Words.Markup](../../aspose.words.markup/)
* asamblea [Aspose.Words](../../)
