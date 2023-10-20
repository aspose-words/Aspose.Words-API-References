---
title: ShowInBalloons Enum
linktitle: ShowInBalloons
articleTitle: ShowInBalloons
second_title: Aspose.Words pour .NET
description: Aspose.Words.Layout.ShowInBalloons énumération. Spécifie quelles révisions sont rendues dans les bulles en C#.
type: docs
weight: 3410
url: /fr/net/aspose.words.layout/showinballoons/
---
## ShowInBalloons enumeration

Spécifie quelles révisions sont rendues dans les bulles.

```csharp
public enum ShowInBalloons
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| None | `0` | Rend les révisions d'insertion, de suppression et de formatage en ligne. |
| Format | `1` | Rend les révisions d'insertion et de suppression en ligne, formate les révisions dans des bulles. |
| FormatAndDelete | `2` | Rend les révisions insérées en ligne, supprimées et formatées dans des bulles. |

## Remarques

Notez que les révisions ne sont pas affichées dans les bulles pourShowInAnnotations .

## Exemples

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

* espace de noms [Aspose.Words.Layout](../../aspose.words.layout/)
* Assemblée [Aspose.Words](../../)
