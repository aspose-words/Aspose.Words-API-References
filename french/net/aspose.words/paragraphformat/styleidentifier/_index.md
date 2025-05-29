---
title: ParagraphFormat.StyleIdentifier
linktitle: StyleIdentifier
articleTitle: StyleIdentifier
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ParagraphFormat StyleIdentifier pour gérer et personnaliser facilement les styles de paragraphe, améliorant ainsi la mise en forme et la lisibilité de votre document.
type: docs
weight: 360
url: /fr/net/aspose.words/paragraphformat/styleidentifier/
---
## ParagraphFormat.StyleIdentifier property

Obtient ou définit l'identifiant de style indépendant des paramètres régionaux du style de paragraphe appliqué à cette mise en forme.

```csharp
public StyleIdentifier StyleIdentifier { get; set; }
```

## Exemples

Montre comment insérer une table des matières (TOC) dans un document en utilisant des styles de titre comme entrées.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérer une table des matières pour la première page du document.
// Configurez le tableau pour récupérer les paragraphes avec des titres de niveaux 1 à 3.
// Définissez également ses entrées comme des hyperliens qui nous mèneront
// à l'emplacement de l'en-tête lors d'un clic gauche dans Microsoft Word.
builder.InsertTableOfContents("\\o \"1-3\" \\h \\z \\u");
builder.InsertBreak(BreakType.PageBreak);

// Remplissez la table des matières en ajoutant des paragraphes avec des styles de titre.
// Chaque titre de ce type avec un niveau compris entre 1 et 3 créera une entrée dans le tableau.
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

* enum [StyleIdentifier](../../styleidentifier/)
* class [ParagraphFormat](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
