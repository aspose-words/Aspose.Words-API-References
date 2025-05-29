---
title: PageSetup.LinesPerPage
linktitle: LinesPerPage
articleTitle: LinesPerPage
second_title: Aspose.Words pour .NET
description: Contrôlez la mise en page de votre document grâce à la propriété PageSetup LinesPerPage. Ajustez facilement le nombre de lignes par page pour une lisibilité et une organisation optimales.
type: docs
weight: 240
url: /fr/net/aspose.words/pagesetup/linesperpage/
---
## PageSetup.LinesPerPage property

Obtient ou définit le nombre de lignes par page dans la grille du document.

```csharp
public int LinesPerPage { get; set; }
```

## Remarques

La valeur minimale de la propriété est 1. La valeur maximale dépend de la hauteur de page et de la taille de police du style Normal . Le pas de ligne minimal est de 136 % de la taille de police. Par exemple, le nombre maximal de lignes par page d'une page Lettre avec des marges d'un pouce est de 39.

Par défaut, la propriété a une valeur dont le pas de ligne est 1,5 fois supérieur à la taille de police du style Normal.

## Exemples

Montre comment spécifier une limite pour le nombre de lignes que chaque page peut contenir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Activez le pitching, puis utilisez-le pour définir le nombre de lignes par page dans cette section.
// Une taille de police suffisamment grande repoussera certaines lignes vers la page suivante pour éviter le chevauchement des caractères.
builder.PageSetup.LayoutMode = SectionLayoutMode.LineGrid;
builder.PageSetup.LinesPerPage = 15;

builder.ParagraphFormat.SnapToGrid = true;

for (int i = 0; i < 30; i++)
    builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");

doc.Save(ArtifactsDir + "PageSetup.LinesPerPage.docx");
```

### Voir également

* class [PageSetup](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
