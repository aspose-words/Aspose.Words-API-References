---
title: StructuredDocumentTag.BuildingBlockCategory
linktitle: BuildingBlockCategory
articleTitle: BuildingBlockCategory
second_title: Aspose.Words per .NET
description: Scopri la proprietà BuildingBlockCategory di StructuredDocumentTag, essenziale per definire le categorie di blocchi predefiniti nei nodi SDT. Migliora la struttura del tuo documento!
type: docs
weight: 30
url: /it/net/aspose.words.markup/structureddocumenttag/buildingblockcategory/
---
## StructuredDocumentTag.BuildingBlockCategory property

Specifica la categoria del blocco di costruzione per questo**SDT** node. Non può essere`null` .

```csharp
public string BuildingBlockCategory { get; set; }
```

## Osservazioni

L'accesso a questa proprietà funzionerà solo perBuildingBlockGallery e DocPartObj Tipi SDT. È di sola lettura per**SDT** del tipo di parte del documento.

Per tutti gli altri tipi di SDT si verificheranno delle eccezioni.

## Esempi

Mostra come inserire un tag di documento strutturato come elemento costitutivo e impostarne la categoria e la galleria.

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
