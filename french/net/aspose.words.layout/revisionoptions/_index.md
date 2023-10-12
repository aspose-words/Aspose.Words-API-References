---
title: Class RevisionOptions
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Layout.RevisionOptions classe. Permet de contrôler la façon dont les révisions du document sont gérées pendant le processus de mise en page.
type: docs
weight: 3390
url: /fr/net/aspose.words.layout/revisionoptions/
---
## RevisionOptions class

Permet de contrôler la façon dont les révisions du document sont gérées pendant le processus de mise en page.

Pour en savoir plus, visitez le[Conversion au format de page fixe](https://docs.aspose.com/words/net/converting-to-fixed-page-format/) article documentaire.

```csharp
public class RevisionOptions
```

## Propriétés

| Nom | La description |
| --- | --- |
| [CommentColor](../../aspose.words.layout/revisionoptions/commentcolor/) { get; set; } | Permet de spécifier la couleur à utiliser pour les commentaires. La valeur par défaut estRed . |
| [DeletedTextColor](../../aspose.words.layout/revisionoptions/deletedtextcolor/) { get; set; } | Permet de spécifier la couleur à utiliser pour le contenu suppriméDeletion . La valeur par défaut estByAuthor . |
| [DeletedTextEffect](../../aspose.words.layout/revisionoptions/deletedtexteffect/) { get; set; } | Permet de préciser l'effet à appliquer au contenu suppriméDeletion . La valeur par défaut estStrikeThrough |
| [InsertedTextColor](../../aspose.words.layout/revisionoptions/insertedtextcolor/) { get; set; } | Permet de spécifier la couleur à utiliser pour le contenu inséréInsertion . La valeur par défaut estByAuthor . |
| [InsertedTextEffect](../../aspose.words.layout/revisionoptions/insertedtexteffect/) { get; set; } | Permet de spécifier l'effet à appliquer au contenu inséréInsertion . La valeur par défaut estUnderline . |
| [MeasurementUnit](../../aspose.words.layout/revisionoptions/measurementunit/) { get; set; } | Permet de spécifier les unités de mesure pour les commentaires de révision. La valeur par défaut estCentimeters |
| [MovedFromTextColor](../../aspose.words.layout/revisionoptions/movedfromtextcolor/) { get; set; } | Permet de spécifier la couleur à utiliser pour les zones d'où le contenu a été déplacéMoving . La valeur par défaut estByAuthor . |
| [MovedFromTextEffect](../../aspose.words.layout/revisionoptions/movedfromtexteffect/) { get; set; } | Permet de spécifier l'effet à appliquer aux zones d'où le contenu a été déplacéMoving . La valeur par défaut estDoubleStrikeThrough |
| [MovedToTextColor](../../aspose.words.layout/revisionoptions/movedtotextcolor/) { get; set; } | Permet de spécifier la couleur à utiliser pour les zones vers lesquelles le contenu a été déplacéMoving . La valeur par défaut estByAuthor . |
| [MovedToTextEffect](../../aspose.words.layout/revisionoptions/movedtotexteffect/) { get; set; } | Permet de spécifier l'effet à appliquer aux zones où le contenu a été déplacéMoving . La valeur par défaut estDoubleUnderline |
| [RevisedPropertiesColor](../../aspose.words.layout/revisionoptions/revisedpropertiescolor/) { get; set; } | Permet de spécifier la couleur à utiliser pour le contenu avec des changements de propriétés de formatageFormatChange La valeur par défaut estNoHighlight . |
| [RevisedPropertiesEffect](../../aspose.words.layout/revisionoptions/revisedpropertieseffect/) { get; set; } | Permet de spécifier l'effet pour les zones de contenu avec des modifications des propriétés de formatageFormatChange La valeur par défaut estNone |
| [RevisionBarsColor](../../aspose.words.layout/revisionoptions/revisionbarscolor/) { get; set; } | Permet de spécifier la couleur à utiliser pour les barres latérales qui identifient les lignes du document contenant des informations révisées. La valeur par défaut estRed . |
| [RevisionBarsPosition](../../aspose.words.layout/revisionoptions/revisionbarsposition/) { get; set; } | Obtient ou définit la position de rendu des barres de révision. La valeur par défaut estOutside . |
| [RevisionBarsWidth](../../aspose.words.layout/revisionoptions/revisionbarswidth/) { get; set; } | Obtient ou définit la largeur des barres de révision, points. |
| [ShowInBalloons](../../aspose.words.layout/revisionoptions/showinballoons/) { get; set; } | Permet de préciser si les révisions sont rendues dans les bulles. La valeur par défaut estNone . |
| [ShowOriginalRevision](../../aspose.words.layout/revisionoptions/showoriginalrevision/) { get; set; } | Permet de spécifier si le texte original doit être affiché au lieu du texte révisé. La valeur par défaut est`FAUX` . |
| [ShowRevisionBars](../../aspose.words.layout/revisionoptions/showrevisionbars/) { get; set; } | Permet de spécifier si les barres de révision doivent être rendues près des lignes contenant du contenu révisé. La valeur par défaut est`vrai` . |
| [ShowRevisionMarks](../../aspose.words.layout/revisionoptions/showrevisionmarks/) { get; set; } | Permet de spécifier si le texte de révision doit être marqué avec un balisage de formatage spécial. La valeur par défaut est`vrai` . |

### Exemples

Montre comment modifier l’apparence des révisions dans un document de sortie rendu.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insère une révision, puis change la couleur de toutes les révisions en vert.
builder.Writeln("This is not a revision.");
doc.StartTrackRevisions("John Doe", DateTime.Now);
builder.Writeln("This is a revision.");
doc.StopTrackRevisions();
builder.Writeln("This is not a revision.");

// Supprime la barre qui apparaît à gauche de chaque ligne révisée.
doc.LayoutOptions.RevisionOptions.InsertedTextColor = RevisionColor.BrightGreen;
doc.LayoutOptions.RevisionOptions.ShowRevisionBars = false;

doc.Save(ArtifactsDir + "Document.LayoutOptionsRevisions.pdf");
```

### Voir également

* espace de noms [Aspose.Words.Layout](../../aspose.words.layout/)
* Assemblée [Aspose.Words](../../)


