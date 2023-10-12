---
title: StructuredDocumentTag.BuildingBlockCategory
second_title: Referencia de API de Aspose.Words para .NET
description: StructuredDocumentTag propiedad. Especifica la categoría del bloque de creación para este TED node. No puede sernulo .
type: docs
weight: 30
url: /es/net/aspose.words.markup/structureddocumenttag/buildingblockcategory/
---
## StructuredDocumentTag.BuildingBlockCategory property

Especifica la categoría del bloque de creación para este **TED** node. No puede ser`nulo` .

```csharp
public string BuildingBlockCategory { get; set; }
```

### Observaciones

Acceder a esta propiedad sólo funcionará paraBuildingBlockGallery y DocPartObj Tipos de TDS. Es de sólo lectura para **TED** del tipo de parte del documento.

Para todos los demás tipos de SDT se producirá una excepción.

### Ejemplos

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
* espacio de nombres [Aspose.Words.Markup](../../structureddocumenttag/)
* asamblea [Aspose.Words](../../../)


