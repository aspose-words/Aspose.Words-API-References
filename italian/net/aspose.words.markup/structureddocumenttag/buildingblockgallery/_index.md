---
title: StructuredDocumentTag.BuildingBlockGallery
linktitle: BuildingBlockGallery
articleTitle: BuildingBlockGallery
second_title: Aspose.Words per .NET
description: StructuredDocumentTag BuildingBlockGallery proprietà. Specifica il tipo di blocco predefinito per questoSDT . Non può esserenullo  in C#.
type: docs
weight: 40
url: /it/net/aspose.words.markup/structureddocumenttag/buildingblockgallery/
---
## StructuredDocumentTag.BuildingBlockGallery property

Specifica il tipo di blocco predefinito per questo**SDT** . Non può essere`nullo` .

```csharp
public string BuildingBlockGallery { get; set; }
```

## Osservazioni

L'accesso a questa proprietà funzionerà solo perBuildingBlockGallery e DocPartObj Tipi SDT. È di sola lettura per**SDT** del tipo di parte del documento.

Per tutti gli altri tipi di SDT si verificherà un'eccezione.

## Esempi

Mostra come inserire un tag di documento strutturato come elemento costitutivo e impostarne la categoria e la raccolta.

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
* spazio dei nomi [Aspose.Words.Markup](../../../aspose.words.markup/)
* assemblea [Aspose.Words](../../../)
