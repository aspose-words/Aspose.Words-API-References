---
title: StructuredDocumentTag.BuildingBlockGallery
linktitle: BuildingBlockGallery
articleTitle: BuildingBlockGallery
second_title: Aspose.Words para .NET
description: StructuredDocumentTag BuildingBlockGallery propiedad. Especifica el tipo de bloque de creación para esteTED . No puede sernulo  en C#.
type: docs
weight: 40
url: /es/net/aspose.words.markup/structureddocumenttag/buildingblockgallery/
---
## StructuredDocumentTag.BuildingBlockGallery property

Especifica el tipo de bloque de creación para este**TED** . No puede ser`nulo` .

```csharp
public string BuildingBlockGallery { get; set; }
```

## Observaciones

Acceder a esta propiedad sólo funcionará paraBuildingBlockGallery y DocPartObj Tipos de TDS. Es de sólo lectura para**TED** del tipo de parte del documento.

Para todos los demás tipos de SDT se producirá una excepción.

## Ejemplos

Muestra cómo insertar una etiqueta de documento estructurado como bloque de construcción y configurar su categoría y galería.

```csharp
Document doc = new Document();

StructuredDocumentTag buildingBlockSdt =
    new StructuredDocumentTag(doc, SdtType.BuildingBlockGallery, MarkupLevel.Block)
    {
        BuildingBlockCategory = "Built-in",
        BuildingBlockGallery = "Table of Contents"
    };

doc.FirstSection.Body.AppendChild(buildingBlockSdt);

doc.Save(ArtifactsDir + "StructuredDocumentTag.BuildingBlockCategories.docx");
```

### Ver también

* class [StructuredDocumentTag](../)
* espacio de nombres [Aspose.Words.Markup](../../../aspose.words.markup/)
* asamblea [Aspose.Words](../../../)
