---
title: Document.PageCount
linktitle: PageCount
articleTitle: PageCount
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Document PageCount, qui révèle le nombre total de pages en fonction de la dernière mise en page, garantissant une gestion et des informations précises sur les documents.
type: docs
weight: 330
url: /fr/net/aspose.words/document/pagecount/
---
## Document.PageCount property

Obtient le nombre de pages du document tel que calculé par l'opération de mise en page la plus récente.

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
// Cette opération n'aura pas besoin d'être refaite lors du rendu du document dans un format d'enregistrement de page fixe,
// comme .pdf. Vous gagnerez ainsi du temps, notamment avec les documents complexes.
doc.Save(ArtifactsDir + "Document.GetPageCount.pdf");
```

### Voir également

* method [UpdatePageLayout](../updatepagelayout/)
* class [Document](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
