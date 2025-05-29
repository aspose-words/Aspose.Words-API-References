---
title: StructuredDocumentTag.BuildingBlockCategory
linktitle: BuildingBlockCategory
articleTitle: BuildingBlockCategory
second_title: Aspose.Words para .NET
description: Descubra la propiedad BuildingBlockCategory de StructuredDocumentTag, esencial para definir categorías de bloques de construcción en nodos SDT. ¡Mejore la estructura de su documento!
type: docs
weight: 30
url: /es/net/aspose.words.markup/structureddocumenttag/buildingblockcategory/
---
## StructuredDocumentTag.BuildingBlockCategory property

Especifica la categoría del bloque de construcción para este**TED** node. No se puede`nulo` .

```csharp
public string BuildingBlockCategory { get; set; }
```

## Observaciones

El acceso a esta propiedad sólo funcionará paraBuildingBlockGallery y DocPartObj Tipos SDT. Es de solo lectura para**TED** del tipo de parte del documento.

Para todos los demás tipos de SDT se producirá una excepción.

## Ejemplos

Muestra cómo insertar una etiqueta de documento estructurado como un bloque de construcción y establecer su categoría y galería.

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
