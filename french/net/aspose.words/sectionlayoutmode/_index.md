---
title: SectionLayoutMode Enum
linktitle: SectionLayoutMode
articleTitle: SectionLayoutMode
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.SectionLayoutMode pour optimiser les mises en page des sections et améliorer le comportement de la grille du document pour un meilleur contrôle du formatage.
type: docs
weight: 6580
url: /fr/net/aspose.words/sectionlayoutmode/
---
## SectionLayoutMode enumeration

Spécifie le mode de mise en page d'une section permettant de définir le comportement de la grille du document.

```csharp
public enum SectionLayoutMode
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Default | `0` | Spécifie qu'aucune grille de document ne doit être appliquée au contenu de la section correspondante dans le document. |
| Grid | `1` | Spécifie que la section correspondante doit avoir à la fois le pas de ligne supplémentaire et le pas de caractère ajoutés à chaque ligne et caractère qu'elle contient afin de maintenir un nombre spécifique de lignes par page et de caractères par ligne. Les caractères ne seront pas automatiquement alignés avec les lignes de la grille lors de la saisie. |
| LineGrid | `2` | Spécifie que la section correspondante doit avoir un espacement de ligne supplémentaire ajouté à chaque ligne qu'elle contient afin de maintenir le nombre spécifié de lignes par page. |
| SnapToChars | `3` | Spécifie que la section correspondante doit avoir à la fois le pas de ligne supplémentaire et le pas de caractère ajoutés à chaque ligne et caractère qu'elle contient afin de maintenir un nombre spécifique de lignes par page et de caractères par ligne. Les caractères seront automatiquement alignés sur le quadrillage lors de la saisie. |

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

* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
