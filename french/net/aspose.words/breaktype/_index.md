---
title: BreakType Enum
linktitle: BreakType
articleTitle: BreakType
second_title: Aspose.Words pour .NET
description: Aspose.Words.BreakType énumération. Spécifie le type de saut à lintérieur dun document en C#.
type: docs
weight: 110
url: /fr/net/aspose.words/breaktype/
---
## BreakType enumeration

Spécifie le type de saut à l'intérieur d'un document.

```csharp
public enum BreakType
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| ParagraphBreak | `0` | Pause entre les paragraphes. |
| PageBreak | `1` | Saut de page explicite. |
| ColumnBreak | `2` | Saut de colonne explicite. |
| SectionBreakContinuous | `3` | Spécifie le début d'une nouvelle section sur la même page que la section précédente. |
| SectionBreakNewColumn | `4` | Spécifie le début d'une nouvelle section dans la nouvelle colonne. |
| SectionBreakNewPage | `5` | Spécifie le début d'une nouvelle section sur une nouvelle page. |
| SectionBreakEvenPage | `6` | Spécifie le début d'une nouvelle section sur une nouvelle page paire. |
| SectionBreakOddPage | `7` | Spécifie le début d'une nouvelle section sur une page impaire. |
| LineBreak | `8` | Saut de ligne explicite. |

## Exemples

Montre comment créer des en-têtes et des pieds de page dans un document à l'aide de DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Spécifie que nous voulons des en-têtes et pieds de page différents pour les premières pages, paires et impaires.
builder.PageSetup.DifferentFirstPageHeaderFooter = true;
builder.PageSetup.OddAndEvenPagesHeaderFooter = true;

// Créez les en-têtes, puis ajoutez trois pages au document pour afficher chaque type d'en-tête.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderFirst);
builder.Write("Header for the first page");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderEven);
builder.Write("Header for even pages");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("Header for all other pages");

builder.MoveToSection(0);
builder.Writeln("Page1");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page2");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page3");

doc.Save(ArtifactsDir + "DocumentBuilder.HeadersAndFooters.docx");
```

Montre comment appliquer et rétablir les paramètres de mise en page aux sections d’un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Modifie les propriétés de mise en page de la section actuelle du générateur et ajoute du texte.
builder.PageSetup.Orientation = Orientation.Landscape;
builder.PageSetup.VerticalAlignment = PageVerticalAlignment.Center;
builder.Writeln("This is the first section, which landscape oriented with vertically centered text.");

// Si on démarre une nouvelle section en utilisant un générateur de documents,
// il héritera des propriétés de mise en page actuelles du constructeur.
builder.InsertBreak(BreakType.SectionBreakNewPage);

Assert.AreEqual(Orientation.Landscape, doc.Sections[1].PageSetup.Orientation);
Assert.AreEqual(PageVerticalAlignment.Center, doc.Sections[1].PageSetup.VerticalAlignment);

// Nous pouvons rétablir ses propriétés de mise en page à leurs valeurs par défaut en utilisant la méthode "ClearFormatting".
builder.PageSetup.ClearFormatting();

Assert.AreEqual(Orientation.Portrait, doc.Sections[1].PageSetup.Orientation);
Assert.AreEqual(PageVerticalAlignment.Top, doc.Sections[1].PageSetup.VerticalAlignment);

builder.Writeln("This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

doc.Save(ArtifactsDir + "PageSetup.ClearFormatting.docx");
```

Montre comment insérer une table des matières (TOC) dans un document en utilisant des styles de titre comme entrées.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insère une table des matières pour la première page du document.
// Configurez le tableau pour récupérer les paragraphes avec des titres de niveaux 1 à 3.
// Définissez également ses entrées comme des hyperliens qui nous amèneront
// à l'emplacement du titre lors d'un clic gauche dans Microsoft Word.
builder.InsertTableOfContents("\\o \"1-3\" \\h \\z \\u");
builder.InsertBreak(BreakType.PageBreak);

// Remplit la table des matières en ajoutant des paragraphes avec des styles de titre.
// Chacun de ces en-têtes avec un niveau compris entre 1 et 3 créera une entrée dans le tableau.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("Heading 2");
builder.Writeln("Heading 3");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 3.1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;
builder.Writeln("Heading 3.1.1");
builder.Writeln("Heading 3.1.2");
builder.Writeln("Heading 3.1.3");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading4;
builder.Writeln("Heading 3.1.3.1");
builder.Writeln("Heading 3.1.3.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 3.2");
builder.Writeln("Heading 3.3");

// Une table des matières est un champ d'un type qui doit être mis à jour pour afficher un résultat à jour.
doc.UpdateFields();
doc.Save(ArtifactsDir + "DocumentBuilder.InsertToc.docx");
```

### Voir également

* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
