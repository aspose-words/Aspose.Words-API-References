---
title: PageSetup.LayoutMode
second_title: Référence de l'API Aspose.Words pour .NET
description: PageSetup propriété. Obtient ou définit le mode de mise en page de cette section.
type: docs
weight: 190
url: /fr/net/aspose.words/pagesetup/layoutmode/
---
## PageSetup.LayoutMode property

Obtient ou définit le mode de mise en page de cette section.

```csharp
public SectionLayoutMode LayoutMode { get; set; }
```

### Exemples

Montre comment spécifier a pour le nombre de caractères que chaque ligne peut avoir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Activez le pas, puis utilisez-le pour définir le nombre de caractères par ligne dans cette section.
builder.PageSetup.LayoutMode = SectionLayoutMode.Grid;
builder.PageSetup.CharactersPerLine = 10;

// Le nombre de caractères dépend également de la taille de la police.
doc.Styles["Normal"].Font.Size = 20;

Assert.AreEqual(8, doc.FirstSection.PageSetup.CharactersPerLine);

builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.Save(ArtifactsDir + "PageSetup.CharactersPerLine.docx");
```

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

* enum [SectionLayoutMode](../../sectionlayoutmode/)
* class [PageSetup](../)
* espace de noms [Aspose.Words](../../pagesetup/)
* Assemblée [Aspose.Words](../../../)


