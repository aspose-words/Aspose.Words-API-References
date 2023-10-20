---
title: IStructuredDocumentTag Interface
linktitle: IStructuredDocumentTag
articleTitle: IStructuredDocumentTag
second_title: Aspose.Words para .NET
description: Aspose.Words.Markup.IStructuredDocumentTag interfaz. Interfaz para definir datos comunes paraStructuredDocumentTag yStructuredDocumentTagRangeStart  en C#.
type: docs
weight: 3970
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
| [Color](../../aspose.words.markup/istructureddocumenttag/color/) { get; set; } | Obtiene o establece el color de la etiqueta del documento estructurado. |
| [Id](../../aspose.words.markup/istructureddocumenttag/id/) { get; } | Especifica una identificación numérica persistente única de solo lectura para esto**TED**. |
| [IsShowingPlaceholderText](../../aspose.words.markup/istructureddocumenttag/isshowingplaceholdertext/) { get; set; } | Especifica si el contenido de este**TED** se interpretará como que contiene el marcador de posición text (a diferencia del contenido de texto normal dentro del SDT). |
| [Level](../../aspose.words.markup/istructureddocumenttag/level/) { get; } | Obtiene el nivel en el que este**TED** ocurre en el árbol del documento. |
| [LockContentControl](../../aspose.words.markup/istructureddocumenttag/lockcontentcontrol/) { get; set; } | Cuando se establece en verdadero, esta propiedad prohibirá que un usuario elimine esto**TED** . |
| [LockContents](../../aspose.words.markup/istructureddocumenttag/lockcontents/) { get; set; } | Cuando se establece en verdadero, esta propiedad prohibirá a un usuario editar el contenido de este**TED** . |
| [Placeholder](../../aspose.words.markup/istructureddocumenttag/placeholder/) { get; } | Obtiene el[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/)que contiene texto de marcador de posición que debe mostrarse cuando el contenido de esta ejecución de SDT está vacío, el elemento XML asignado asociado está vacío como se especifica mediante el[`XmlMapping`](./xmlmapping/) element o el[`IsShowingPlaceholderText`](./isshowingplaceholdertext/) elemento es verdadero. |
| [PlaceholderName](../../aspose.words.markup/istructureddocumenttag/placeholdername/) { get; set; } | Obtiene o establece el nombre del[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/) que contiene texto de marcador de posición. |
| [SdtType](../../aspose.words.markup/istructureddocumenttag/sdttype/) { get; } | Obtiene el tipo de esto**Etiqueta de documento estructurado** . |
| [Tag](../../aspose.words.markup/istructureddocumenttag/tag/) { get; set; } | Especifica una etiqueta asociada con el nodo SDT actual. No puede ser nulo. |
| [Title](../../aspose.words.markup/istructureddocumenttag/title/) { get; set; } | Especifica el nombre descriptivo asociado con este**TED** . No puede ser nulo. |
| [WordOpenXML](../../aspose.words.markup/istructureddocumenttag/wordopenxml/) { get; } | Obtiene una cadena que representa el XML contenido dentro del nodo en elFlatOpc formato. |
| [XmlMapping](../../aspose.words.markup/istructureddocumenttag/xmlmapping/) { get; } | Obtiene un objeto que representa la asignación de esta etiqueta de documento estructurado a datos XML en una parte XML personalizada del documento actual. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [IsRanged](../../aspose.words.markup/istructureddocumenttag/isranged/)() | Devuelve verdadero si esta instancia es una etiqueta de documento estructurado por rangos. |
| [StructuredDocumentTagNode](../../aspose.words.markup/istructureddocumenttag/structureddocumenttagnode/)() | Devuelve el objeto Nodo que implementa esta interfaz. |

### Ver también

* espacio de nombres [Aspose.Words.Markup](../../aspose.words.markup/)
* asamblea [Aspose.Words](../../)
