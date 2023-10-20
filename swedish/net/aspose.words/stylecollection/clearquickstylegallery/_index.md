---
title: StyleCollection.ClearQuickStyleGallery
linktitle: ClearQuickStyleGallery
articleTitle: ClearQuickStyleGallery
second_title: Aspose.Words för .NET
description: StyleCollection ClearQuickStyleGallery metod. Tar bort alla stilar från panelen Quick Style Gallery i C#.
type: docs
weight: 80
url: /sv/net/aspose.words/stylecollection/clearquickstylegallery/
---
## StyleCollection.ClearQuickStyleGallery method

Tar bort alla stilar från panelen Quick Style Gallery.

```csharp
public void ClearQuickStyleGallery()
```

## Exempel

Visar hur du tar bort stilar från Style Gallery-panelen.

```csharp
Document doc = new Document();
// Observera att borttagningsstilar endast fungerar med DOCX-format för närvarande.
doc.Styles.ClearQuickStyleGallery();

doc.Save(ArtifactsDir + "Styles.RemoveStylesFromStyleGallery.docx");
```

### Se även

* class [StyleCollection](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
