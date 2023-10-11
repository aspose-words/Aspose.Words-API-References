---
title: RevisionOptions.MovedFromTextColor
second_title: Référence de l'API Aspose.Words pour .NET
description: RevisionOptions propriété. Permet de spécifier la couleur à utiliser pour les zones doù le contenu a été déplacéMoving . La valeur par défaut estByAuthor .
type: docs
weight: 70
url: /fr/net/aspose.words.layout/revisionoptions/movedfromtextcolor/
---
## RevisionOptions.MovedFromTextColor property

Permet de spécifier la couleur à utiliser pour les zones d'où le contenu a été déplacéMoving . La valeur par défaut estByAuthor .

```csharp
public RevisionColor MovedFromTextColor { get; set; }
```

### Exemples

Montre comment modifier l’apparence des révisions.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

// Récupère l'objet RevisionOptions qui contrôle l'apparence des révisions.
RevisionOptions revisionOptions = doc.LayoutOptions.RevisionOptions;

// Rendre les révisions d'insertion en vert et en italique.
revisionOptions.InsertedTextColor = RevisionColor.Green;
revisionOptions.InsertedTextEffect = RevisionTextEffect.Italic;

// Afficher les révisions de suppression en rouge et en gras.
revisionOptions.DeletedTextColor = RevisionColor.Red;
revisionOptions.DeletedTextEffect = RevisionTextEffect.Bold;

// Le même texte apparaîtra deux fois dans une révision de mouvement :
// une fois au point de départ et une fois à la destination d'arrivée.
// Rend le texte à la révision déplacée en jaune avec un double barré
// et bleu doublement souligné à la révision déplacée.
revisionOptions.MovedFromTextColor = RevisionColor.Yellow;
revisionOptions.MovedFromTextEffect = RevisionTextEffect.DoubleStrikeThrough;
revisionOptions.MovedToTextColor = RevisionColor.ClassicBlue;
revisionOptions.MovedFromTextEffect = RevisionTextEffect.DoubleUnderline;

// Rendu des révisions de format en rouge foncé et gras.
revisionOptions.RevisedPropertiesColor = RevisionColor.DarkRed;
revisionOptions.RevisedPropertiesEffect = RevisionTextEffect.Bold;

// Place une barre bleue foncée épaisse sur le côté gauche de la page à côté des lignes affectées par les révisions.
revisionOptions.RevisionBarsColor = RevisionColor.DarkBlue;
revisionOptions.RevisionBarsWidth = 15.0f;

// Afficher les marques de révision et le texte original.
revisionOptions.ShowOriginalRevision = true;
revisionOptions.ShowRevisionMarks = true;

// Obtenez le mouvement, la suppression, les révisions de formatage et les commentaires à afficher dans des bulles vertes
// sur le côté droit de la page.
revisionOptions.ShowInBalloons = ShowInBalloons.Format;
revisionOptions.CommentColor = RevisionColor.BrightGreen;

// Ces fonctionnalités ne sont applicables qu'aux formats tels que .pdf ou .jpg.
doc.Save(ArtifactsDir + "Revision.RevisionOptions.pdf");
```

### Voir également

* enum [RevisionColor](../../revisioncolor/)
* class [RevisionOptions](../)
* espace de noms [Aspose.Words.Layout](../../revisionoptions/)
* Assemblée [Aspose.Words](../../../)


