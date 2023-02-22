---
title: RevisionOptions.ShowInBalloons
second_title: Référence de l'API Aspose.Words pour .NET
description: RevisionOptions propriété. Permet de spécifier si les révisions sont rendues dans les bulles. La valeur par défaut estNone .
type: docs
weight: 160
url: /fr/net/aspose.words.layout/revisionoptions/showinballoons/
---
## RevisionOptions.ShowInBalloons property

Permet de spécifier si les révisions sont rendues dans les bulles. La valeur par défaut estNone .

```csharp
public ShowInBalloons ShowInBalloons { get; set; }
```

### Remarques

Notez que les révisions ne sont pas affichées dans des bulles pourShowInAnnotations .

### Exemples

Montre comment afficher les révisions dans des bulles.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

// Par défaut, le texte qui est une révision a une couleur différente pour le différencier de l'autre texte non révisé.
// Définissez une option de révision pour afficher plus de détails sur chaque révision dans une bulle sur la marge droite de la page.
doc.LayoutOptions.RevisionOptions.ShowInBalloons = ShowInBalloons.FormatAndDelete;
doc.Save(ArtifactsDir + "Revision.ShowRevisionBalloons.pdf");
```

Montre comment modifier l'apparence des révisions.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

// Récupère l'objet RevisionOptions qui contrôle l'apparence des révisions.
RevisionOptions revisionOptions = doc.LayoutOptions.RevisionOptions;

// Affiche les révisions d'insertion en vert et en italique.
revisionOptions.InsertedTextColor = RevisionColor.Green;
revisionOptions.InsertedTextEffect = RevisionTextEffect.Italic;

// Afficher les révisions de suppression en rouge et en gras.
revisionOptions.DeletedTextColor = RevisionColor.Red;
revisionOptions.DeletedTextEffect = RevisionTextEffect.Bold;

// Le même texte apparaîtra deux fois dans une révision de mouvement :
// une fois au point de départ et une fois à la destination d'arrivée.
// Rendre le texte à la révision d'origine jaune avec un double barré
// et bleu souligné deux fois à la révision déplacée vers.
revisionOptions.MovedFromTextColor = RevisionColor.Yellow;
revisionOptions.MovedFromTextEffect = RevisionTextEffect.DoubleStrikeThrough;
revisionOptions.MovedToTextColor = RevisionColor.Blue;
revisionOptions.MovedFromTextEffect = RevisionTextEffect.DoubleUnderline;

// Afficher les révisions de format en rouge foncé et en gras.
revisionOptions.RevisedPropertiesColor = RevisionColor.DarkRed;
revisionOptions.RevisedPropertiesEffect = RevisionTextEffect.Bold;

// Place une épaisse barre bleu foncé sur le côté gauche de la page à côté des lignes affectées par les révisions.
revisionOptions.RevisionBarsColor = RevisionColor.DarkBlue;
revisionOptions.RevisionBarsWidth = 15.0f;

// Affiche les marques de révision et le texte d'origine.
revisionOptions.ShowOriginalRevision = true;
revisionOptions.ShowRevisionMarks = true;

// Obtenez le mouvement, la suppression, les révisions de formatage et les commentaires à afficher dans des bulles vertes
// sur le côté droit de la page.
revisionOptions.ShowInBalloons = ShowInBalloons.Format;
revisionOptions.CommentColor = RevisionColor.BrightGreen;

// Ces fonctionnalités ne s'appliquent qu'aux formats tels que .pdf ou .jpg.
doc.Save(ArtifactsDir + "Revision.RevisionOptions.pdf");
```

### Voir également

* enum [ShowInBalloons](../../showinballoons/)
* class [RevisionOptions](../)
* espace de noms [Aspose.Words.Layout](../../revisionoptions/)
* Assemblée [Aspose.Words](../../../)


