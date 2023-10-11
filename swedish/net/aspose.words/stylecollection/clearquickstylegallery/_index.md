---
title: StyleCollection.ClearQuickStyleGallery
second_title: Aspose.Words för .NET API Referens
description: StyleCollection metod. Tar bort alla stilar från panelen Quick Style Gallery.
type: docs
weight: 80
url: /sv/net/aspose.words/stylecollection/clearquickstylegallery/
---
## StyleCollection.ClearQuickStyleGallery method

Tar bort alla stilar från panelen Quick Style Gallery.

```csharp
public void ClearQuickStyleGallery()
```

### Exempel

Visar hur du tar bort stilar från Style Gallery-panelen.

```csharp
Document doc = new Document();
// Observera att borttagningsstilar endast fungerar med DOCX-format för närvarande.
doc.Styles.ClearQuickStyleGallery();

doc.Save(ArtifactsDir + "Styles.RemoveStylesFromStyleGallery.docx");
```

### Se även

* class [StyleCollection](../)
* namnutrymme [Aspose.Words](../../stylecollection/)
* hopsättning [Aspose.Words](../../../)


