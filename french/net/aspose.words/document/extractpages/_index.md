---
title: Document.ExtractPages
linktitle: ExtractPages
articleTitle: ExtractPages
second_title: Aspose.Words pour .NET
description: Découvrez la méthode Document ExtractPages pour récupérer sans effort des plages de pages spécifiques, améliorant ainsi la gestion et l'efficacité de vos documents.
type: docs
weight: 640
url: /fr/net/aspose.words/document/extractpages/
---
## Document.ExtractPages method

Renvoie le[`Document`](../) objet représentant une plage de pages spécifiée.

```csharp
public Document ExtractPages(int index, int count)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| index | Int32 | L'index de base zéro de la première page à extraire. |
| count | Int32 | Nombre de pages à extraire. |

## Remarques

Le document résultant devrait ressembler à celui de MS Word, comme si nous avions effectué « Imprimer des pages spécifiques » ; la numérotation, les en-têtes/pieds de page et la mise en page des tableaux croisés seront conservés. Cependant, en raison du grand nombre de nuances apparaissant lors de la réduction du nombre de pages, la correspondance complète de la mise en page est une tâche assez compliquée qui demande beaucoup d'efforts. Selon la complexité du document, il peut y avoir de légères différences dans la mise en page du contenu du document résultant par rapport au document source. Tout commentaire serait grandement apprécié.

## Exemples

Montre comment obtenir une plage de pages spécifiée à partir du document.

```csharp
Document doc = new Document(MyDir + "Layout entities.docx");

doc = doc.ExtractPages(0, 2);

doc.Save(ArtifactsDir + "Document.ExtractPages.docx");
```

### Voir également

* class [Document](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
