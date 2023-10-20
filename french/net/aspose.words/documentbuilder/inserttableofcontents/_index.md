---
title: DocumentBuilder.InsertTableOfContents
linktitle: InsertTableOfContents
articleTitle: InsertTableOfContents
second_title: Aspose.Words pour .NET
description: DocumentBuilder InsertTableOfContents méthode. Insère un champ TOC table des matières dans le document en C#.
type: docs
weight: 460
url: /fr/net/aspose.words/documentbuilder/inserttableofcontents/
---
## DocumentBuilder.InsertTableOfContents method

Insère un champ TOC (table des matières) dans le document.

```csharp
public Field InsertTableOfContents(string switches)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| switches | String | Le champ TOC change. |

## Remarques

Cette méthode insère un champ TOC (table des matières) dans le document à la position actuelle.

Une table des matières dans un document Word peut être créée de plusieurs manières et formatée à l'aide de diverses options. La façon dont le tableau est construit et affiché par Microsoft Word est contrôlée par les commutateurs de champ.

Le moyen le plus simple de spécifier les commutateurs est d'insérer et de configurer une table de contenu dans un document Word à l'aide du menu Insertion-&gt;Référence-&gt;Index et tableaux, , puis d'activer l'affichage des codes de champ pour voir les commutateurs. Vous pouvez appuyer sur Alt+F9 dans Microsoft Word pour activer ou désactiver l'affichage des codes de champ.

Par exemple, après avoir créé une table des matières, le champ suivant est inséré dans le document :**{ Table des matières \o "1-3" \h \z \u }** . Vous pouvez copier**\o "1-3" \h \z \u** et utilisez-le comme paramètre de commutateurs.

Noter que`InsertTableOfContents` insérera uniquement un champ TOC, mais ne construira pas réellement la table des matières. La table des matières est construite par Microsoft Word lorsque le champ est mis à jour.

Si vous insérez une table des matières à l'aide de cette méthode, puis ouvrez le fichier dans Microsoft Word, vous ne verrez pas la table des matières car le champ TOC n'a pas encore été mis à jour.

Dans Microsoft Word, les champs ne sont pas automatiquement mis à jour lorsqu'un document est ouvert, mais vous pouvez mettre à jour les champs d'un document à tout moment en appuyant sur F9.

## Exemples

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

* class [Field](../../../aspose.words.fields/field/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
