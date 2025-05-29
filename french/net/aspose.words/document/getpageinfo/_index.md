---
title: Document.GetPageInfo
linktitle: GetPageInfo
articleTitle: GetPageInfo
second_title: Aspose.Words pour .NET
description: Découvrez la méthode GetPageInfo pour récupérer les détails essentiels de taille, d'orientation et de rendu de page pour une impression optimisée et une gestion améliorée des documents.
type: docs
weight: 650
url: /fr/net/aspose.words/document/getpageinfo/
---
## Document.GetPageInfo method

Obtient la taille de la page, l'orientation et d'autres informations sur une page qui pourraient être utiles pour l'impression ou le rendu.

```csharp
public PageInfo GetPageInfo(int pageIndex)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| pageIndex | Int32 | L'index de page basé sur 0. |

## Exemples

Montre comment vérifier si la page est en couleur ou non.

```csharp
Document doc = new Document(MyDir + "Document.docx");

// Vérifiez que la première page du document n'est pas colorée.
Assert.IsFalse(doc.GetPageInfo(0).Colored);
```

### Voir également

* class [PageInfo](../../../aspose.words.rendering/pageinfo/)
* class [Document](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
