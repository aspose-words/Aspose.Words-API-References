---
title: OutlineOptions.ExpandedOutlineLevels
linktitle: ExpandedOutlineLevels
articleTitle: ExpandedOutlineLevels
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ExpandedOutlineLevels dans OutlineOptions, vous permettant de personnaliser la visibilité du plan du document pour une navigation et une expérience utilisateur améliorées.
type: docs
weight: 60
url: /fr/net/aspose.words.saving/outlineoptions/expandedoutlinelevels/
---
## OutlineOptions.ExpandedOutlineLevels property

Spécifie le nombre de niveaux dans le plan du document à afficher développés lorsque le fichier est visualisé.

```csharp
public int ExpandedOutlineLevels { get; set; }
```

## Remarques

Notez que ces options ne fonctionneront pas lors de l'enregistrement au format XPS.

Spécifiez 0 et le plan du document sera réduit ; spécifiez 1 et les éléments de premier niveau dans le plan seront développés et ainsi de suite.

La valeur par défaut est 0. La plage valide est de 0 à 9.

## Exemples

Montre comment convertir un document entier en PDF avec trois niveaux dans le plan du document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérer les titres des niveaux 1 à 5.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;

builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;

builder.Writeln("Heading 1.2.1");
builder.Writeln("Heading 1.2.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading4;

builder.Writeln("Heading 1.2.2.1");
builder.Writeln("Heading 1.2.2.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading5;

builder.Writeln("Heading 1.2.2.2.1");
builder.Writeln("Heading 1.2.2.2.2");

// Créez un objet « PdfSaveOptions » que nous pouvons transmettre à la méthode « Save » du document
// pour modifier la manière dont cette méthode convertit le document en .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Le document PDF de sortie contiendra un plan, qui est une table des matières répertoriant les titres dans le corps du document.
// Cliquer sur une entrée dans ce plan nous amènera à l'emplacement de son titre respectif.
// Définissez la propriété « HeadingsOutlineLevels » sur « 4 » pour exclure tous les titres dont les niveaux sont supérieurs à 4 du plan.
options.OutlineOptions.HeadingsOutlineLevels = 4;

// Si une entrée de plan comporte des entrées ultérieures d'un niveau supérieur entre elle-même et l'entrée suivante du même niveau ou d'un niveau inférieur,
// Une flèche apparaîtra à gauche de l'entrée. Cette entrée est le « propriétaire » de plusieurs « sous-entrées ».
// Dans notre document, les entrées de plan du 5ème niveau de titre sont des sous-entrées de la deuxième entrée de plan du 4ème niveau,
// les entrées de niveau 4 et 5 sont des sous-entrées de la deuxième entrée de niveau 3, et ainsi de suite.
// Dans le plan, nous pouvons cliquer sur la flèche de l'entrée « propriétaire » pour réduire/développer toutes ses sous-entrées.
// Définissez la propriété « ExpandedOutlineLevels » sur « 2 » pour développer automatiquement toutes les entrées de plan de niveau 2 et inférieur
// et réduire toutes les entrées de niveau 3 et supérieur lorsque nous ouvrons le document.
options.OutlineOptions.ExpandedOutlineLevels = 2;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExpandedOutlineLevels.pdf", options);
```

### Voir également

* class [OutlineOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
