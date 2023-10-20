---
title: Document.PageCount
linktitle: PageCount
articleTitle: PageCount
second_title: Aspose.Words pour .NET
description: Document PageCount propriété. Obtient le nombre de pages du document calculé par lopération de mise en page la plus récente en C#.
type: docs
weight: 320
url: /fr/net/aspose.words/document/pagecount/
---
## Document.PageCount property

Obtient le nombre de pages du document calculé par l'opération de mise en page la plus récente.

```csharp
public int PageCount { get; }
```

## Exemples

Montre comment compter le nombre de pages dans le document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Page 1");
builder.InsertBreak(BreakType.PageBreak);
builder.Write("Page 2");
builder.InsertBreak(BreakType.PageBreak);
builder.Write("Page 3");

// Vérifiez le nombre de pages attendu du document.
Assert.AreEqual(3, doc.PageCount);

// L'obtention de la propriété PageCount a invoqué la mise en page du document pour calculer la valeur.
// Cette opération n'aura pas besoin d'être refaite lors du rendu du document dans un format de sauvegarde de page fixe,
// tel que .pdf. Vous pouvez ainsi gagner du temps, notamment avec des documents plus complexes.
doc.Save(ArtifactsDir + "Document.GetPageCount.pdf");
```

### Voir également

* method [UpdatePageLayout](../updatepagelayout/)
* class [Document](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
