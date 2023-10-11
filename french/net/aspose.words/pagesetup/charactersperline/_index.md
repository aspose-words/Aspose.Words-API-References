---
title: PageSetup.CharactersPerLine
second_title: Référence de l'API Aspose.Words pour .NET
description: PageSetup propriété. Obtient ou définit le nombre de caractères par ligne dans la grille du document.
type: docs
weight: 100
url: /fr/net/aspose.words/pagesetup/charactersperline/
---
## PageSetup.CharactersPerLine property

Obtient ou définit le nombre de caractères par ligne dans la grille du document.

```csharp
public int CharactersPerLine { get; set; }
```

### Remarques

La valeur minimale de la propriété est 1. La valeur maximale dépend de la largeur de la page et de la taille de la police du style Normal . L'espacement minimum des caractères est de 90 pour cent de la taille de la police. Par exemple, le nombre maximum de caractères par ligne d'une page Lettre avec des marges d'un pouce est de 43.

Par défaut, la propriété a une valeur sur laquelle le pas des caractères est égal à la taille de la police du style Normal .

### Exemples

Montre comment spécifier a pour le nombre de caractères que chaque ligne peut contenir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Activez le pitch, puis utilisez-le pour définir le nombre de caractères par ligne dans cette section.
builder.PageSetup.LayoutMode = SectionLayoutMode.Grid;
builder.PageSetup.CharactersPerLine = 10;

// Le nombre de caractères dépend également de la taille de la police.
doc.Styles["Normal"].Font.Size = 20;

Assert.AreEqual(8, doc.FirstSection.PageSetup.CharactersPerLine);

builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.Save(ArtifactsDir + "PageSetup.CharactersPerLine.docx");
```

### Voir également

* class [PageSetup](../)
* espace de noms [Aspose.Words](../../pagesetup/)
* Assemblée [Aspose.Words](../../../)


