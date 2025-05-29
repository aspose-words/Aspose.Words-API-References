---
title: PageSetup.CharactersPerLine
linktitle: CharactersPerLine
articleTitle: CharactersPerLine
second_title: Aspose.Words pour .NET
description: Contrôlez la mise en page de votre document avec la propriété CaractèresParLigne de PageSetup. Ajustez facilement le nombre de caractères par ligne pour une lisibilité et une mise en page optimales.
type: docs
weight: 100
url: /fr/net/aspose.words/pagesetup/charactersperline/
---
## PageSetup.CharactersPerLine property

Obtient ou définit le nombre de caractères par ligne dans la grille du document.

```csharp
public int CharactersPerLine { get; set; }
```

## Remarques

La valeur minimale de la propriété est 1. Sa valeur maximale dépend de la largeur de la page et de la taille de police du style Normal . L'espacement minimal des caractères est de 90 % de la taille de police. Par exemple, le nombre maximal de caractères par ligne d'une page Lettre avec des marges d'un pouce est de 43.

Par défaut, la propriété a une valeur dont la hauteur de caractère est égale à la taille de police du style Normal .

## Exemples

Montre comment spécifier un pour le nombre de caractères que chaque ligne peut avoir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Activez le pitching, puis utilisez-le pour définir le nombre de caractères par ligne dans cette section.
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
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
