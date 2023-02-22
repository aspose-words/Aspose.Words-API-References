---
title: StructuredDocumentTag.BuildingBlockCategory
second_title: Aspose.Words per .NET API Reference
description: StructuredDocumentTag proprietà. Specifica la categoria del building block per questo SDT node. Non può essere null.
type: docs
weight: 30
url: /it/net/aspose.words.markup/structureddocumenttag/buildingblockcategory/
---
## StructuredDocumentTag.BuildingBlockCategory property

Specifica la categoria del building block per questo **SDT** node. Non può essere null.

```csharp
public string BuildingBlockCategory { get; set; }
```

### Osservazioni

L'accesso a questa proprietà funzionerà solo perBuildingBlockGallery e DocPartObj Tipi di SDT. È di sola lettura per **SDT**del tipo di parte del documento.

Per tutti gli altri tipi di SDT si verificherà un'eccezione.

### Esempi

Mostra come inserire un tag di documento strutturato come blocco predefinito e impostarne la categoria e la galleria.

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

### Guarda anche

* class [StructuredDocumentTag](../)
* spazio dei nomi [Aspose.Words.Markup](../../structureddocumenttag/)
* assemblea [Aspose.Words](../../../)


