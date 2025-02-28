---
title: StyleCollection.ClearQuickStyleGallery
linktitle: ClearQuickStyleGallery
articleTitle: ClearQuickStyleGallery
second_title: Aspose.Words for .NET
description: Effortlessly clear styles from your Quick Style Gallery with StyleCollection's ClearQuickStyleGallery method. Simplify your design process today!
type: docs
weight: 80
url: /net/aspose.words/stylecollection/clearquickstylegallery/
---
## StyleCollection.ClearQuickStyleGallery method

Removes all styles from the Quick Style Gallery panel.

```csharp
public void ClearQuickStyleGallery()
```

## Examples

Shows how to remove styles from Style Gallery panel.

```csharp
Document doc = new Document();
// Note that remove styles work only with DOCX format for now.
doc.Styles.ClearQuickStyleGallery();

doc.Save(ArtifactsDir + "Styles.RemoveStylesFromStyleGallery.docx");
```

### See Also

* class [StyleCollection](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
