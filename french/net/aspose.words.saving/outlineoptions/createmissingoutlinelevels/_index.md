---
title: OutlineOptions.CreateMissingOutlineLevels
linktitle: CreateMissingOutlineLevels
articleTitle: CreateMissingOutlineLevels
second_title: Aspose.Words pour .NET
description: OutlineOptions CreateMissingOutlineLevels propriété. Obtient ou définit une valeur déterminant sil faut ou non créer des niveaux hiérarchiques manquants lorsque le document est exporté en C#.
type: docs
weight: 30
url: /fr/net/aspose.words.saving/outlineoptions/createmissingoutlinelevels/
---
## OutlineOptions.CreateMissingOutlineLevels property

Obtient ou définit une valeur déterminant s'il faut ou non créer des niveaux hiérarchiques manquants lorsque le document est exporté.

La valeur par défaut de cette propriété est`FAUX`.

```csharp
public bool CreateMissingOutlineLevels { get; set; }
```

## Exemples

Montre comment travailler avec des niveaux hiérarchiques qui ne contiennent aucun titre correspondant lors de l'enregistrement d'un document PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insère des titres pouvant servir d'entrées de table des matières des niveaux 1 et 5.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading5;

builder.Writeln("Heading 1.1.1.1.1");
builder.Writeln("Heading 1.1.1.1.2");

// Crée un objet "PdfSaveOptions" que l'on peut passer à la méthode "Save" du document
// pour modifier la façon dont cette méthode convertit le document en .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Le document PDF de sortie contiendra un plan, qui est une table des matières répertoriant les titres dans le corps du document.
// Cliquer sur une entrée de ce plan nous amènera à l'emplacement de son en-tête respectif.
// Définissez la propriété "HeadingsOutlineLevels" sur "5" pour inclure tous les titres des niveaux 5 et inférieurs dans le plan.
saveOptions.OutlineOptions.HeadingsOutlineLevels = 5;

// Ce document contient des titres de niveaux 1 et 5, et aucun titre de niveaux 2, 3 et 4.
// Le document PDF de sortie traitera les niveaux de plan 2, 3 et 4 comme "manquants".
// Fixe la propriété "CreateMissingOutlineLevels" à "true" pour inclure tous les niveaux manquants dans le plan,
// laissant les entrées de plan vides car il n'y a pas de titres utilisables.
// Fixe la propriété "CreateMissingOutlineLevels" à "false" pour ignorer les niveaux hiérarchiques manquants,
// et traite les titres du plan de niveau 5 comme étant de niveau 2.
saveOptions.OutlineOptions.CreateMissingOutlineLevels = createMissingOutlineLevels;

doc.Save(ArtifactsDir + "PdfSaveOptions.CreateMissingOutlineLevels.pdf", saveOptions);
```

### Voir également

* class [OutlineOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
