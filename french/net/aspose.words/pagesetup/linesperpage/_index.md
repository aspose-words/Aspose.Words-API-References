---
title: PageSetup.LinesPerPage
second_title: Référence de l'API Aspose.Words pour .NET
description: PageSetup propriété. Obtient ou définit le nombre de lignes par page dans la grille du document.
type: docs
weight: 240
url: /fr/net/aspose.words/pagesetup/linesperpage/
---
## PageSetup.LinesPerPage property

Obtient ou définit le nombre de lignes par page dans la grille du document.

```csharp
public int LinesPerPage { get; set; }
```

### Remarques

La valeur minimale de la propriété est 1. La valeur maximale dépend de la hauteur de page et de la taille de police du style Normal . Le pas de ligne minimum est de 136 % de la taille de la police. Par exemple, le nombre maximum de lignes par page de une page Lettre avec des marges d'un pouce est de 39.

Par défaut, la propriété a une valeur sur laquelle le pas de ligne est 1,5 fois supérieur à la taille de police de du style Normal.

### Exemples

Montre comment spécifier une limite pour le nombre de lignes que chaque page peut avoir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Activez le pitching, puis utilisez-le pour définir le nombre de lignes par page dans cette section.
// Une taille de police suffisamment grande poussera certaines lignes vers le bas sur la page suivante pour éviter les caractères qui se chevauchent.
builder.PageSetup.LayoutMode = SectionLayoutMode.LineGrid;
builder.PageSetup.LinesPerPage = 15;

builder.ParagraphFormat.SnapToGrid = true;

for (int i = 0; i < 30; i++)
    builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");

doc.Save(ArtifactsDir + "PageSetup.LinesPerPage.docx");
```

### Voir également

* class [PageSetup](../)
* espace de noms [Aspose.Words](../../pagesetup/)
* Assemblée [Aspose.Words](../../../)


