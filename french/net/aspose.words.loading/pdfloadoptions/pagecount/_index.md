---
title: PdfLoadOptions.PageCount
linktitle: PageCount
articleTitle: PageCount
second_title: Aspose.Words pour .NET
description: Contrôlez la lecture des pages avec la propriété PageCount de PdfLoadOptions. Définissez facilement le nombre de pages à lire pour une gestion efficace des documents.
type: docs
weight: 20
url: /fr/net/aspose.words.loading/pdfloadoptions/pagecount/
---
## PdfLoadOptions.PageCount property

Récupère ou définit le nombre de pages à lire. La valeur par défaut est MaxValue, ce qui signifie que toutes les pages du document seront lues.

```csharp
public int PageCount { get; set; }
```

## Exemples

Montre comment ignorer les images lors du chargement des fichiers PDF.

```csharp
PdfLoadOptions options = new PdfLoadOptions();
options.SkipPdfImages = isSkipPdfImages;
options.PageIndex = 0;
options.PageCount = 1;

Document doc = new Document(MyDir + "Images.pdf", options);
NodeCollection shapeCollection = doc.GetChildNodes(NodeType.Shape, true);

if (isSkipPdfImages)
    Assert.AreEqual(shapeCollection.Count, 0);
else
    Assert.AreNotEqual(shapeCollection.Count, 0);
```

### Voir également

* class [PdfLoadOptions](../)
* espace de noms [Aspose.Words.Loading](../../../aspose.words.loading/)
* Assemblée [Aspose.Words](../../../)
