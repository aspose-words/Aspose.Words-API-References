---
title: PdfLoadOptions.PageIndex
linktitle: PageIndex
articleTitle: PageIndex
second_title: Aspose.Words pour .NET
description: Découvrez PdfLoadOptions PageIndex. Définissez facilement l'index de la page de départ pour la lecture de PDF grâce à cette propriété flexible. Optimisez la gestion de vos PDF dès aujourd'hui !
type: docs
weight: 30
url: /fr/net/aspose.words.loading/pdfloadoptions/pageindex/
---
## PdfLoadOptions.PageIndex property

Obtient ou définit l'index (à partir de 0) de la première page à lire. La valeur par défaut est 0.

```csharp
public int PageIndex { get; set; }
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
