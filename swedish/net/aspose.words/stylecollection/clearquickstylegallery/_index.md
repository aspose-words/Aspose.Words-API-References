---
title: StyleCollection.ClearQuickStyleGallery
linktitle: ClearQuickStyleGallery
articleTitle: ClearQuickStyleGallery
second_title: Aspose.Words för .NET
description: Rensa enkelt stilar från ditt Quick Style Gallery med StyleCollections ClearQuickStyleGallery-metod. Förenkla din designprocess idag!
type: docs
weight: 80
url: /sv/net/aspose.words/stylecollection/clearquickstylegallery/
---
## StyleCollection.ClearQuickStyleGallery method

Tar bort alla stilar från panelen Snabbstilsgalleri.

```csharp
public void ClearQuickStyleGallery()
```

## Exempel

Visar hur man tar bort stilar från panelen Stilgalleri.

```csharp
Document doc = new Document();
// Observera att borttagning av stilar för närvarande endast fungerar med DOCX-format.
doc.Styles.ClearQuickStyleGallery();

doc.Save(ArtifactsDir + "Styles.RemoveStylesFromStyleGallery.docx");
```

### Se även

* class [StyleCollection](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
