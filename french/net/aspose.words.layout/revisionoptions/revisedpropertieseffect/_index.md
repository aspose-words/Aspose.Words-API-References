---
title: RevisionOptions.RevisedPropertiesEffect
linktitle: RevisedPropertiesEffect
articleTitle: RevisedPropertiesEffect
second_title: Aspose.Words pour .NET
description: Découvrez comment l'effet RevisedPropertiesEffect de RevisionOptions améliore la mise en forme de votre contenu. Personnalisez facilement les modifications grâce à la fonctionnalité FormatChange.
type: docs
weight: 140
url: /fr/net/aspose.words.layout/revisionoptions/revisedpropertieseffect/
---
## RevisionOptions.RevisedPropertiesEffect property

Permet de spécifier l'effet pour les zones de contenu avec des modifications des propriétés de formatageFormatChange La valeur par défaut estNone

```csharp
public RevisionTextEffect RevisedPropertiesEffect { get; set; }
```

### Exceptions

| exception | condition |
| --- | --- |
| ArgumentOutOfRangeException | Hidden n'est pas autorisé. |

## Exemples

Montre comment modifier l'apparence des révisions.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

// Obtenez l'objet RevisionOptions qui contrôle l'apparence des révisions.
RevisionOptions revisionOptions = doc.LayoutOptions.RevisionOptions;

// Rendre les révisions d'insertion en vert et en italique.
revisionOptions.InsertedTextColor = RevisionColor.Green;
revisionOptions.InsertedTextEffect = RevisionTextEffect.Italic;

// Rendre les révisions de suppression en rouge et en gras.
revisionOptions.DeletedTextColor = RevisionColor.Red;
revisionOptions.DeletedTextEffect = RevisionTextEffect.Bold;

// Le même texte apparaîtra deux fois dans une révision de mouvement :
// une fois au point de départ et une fois à la destination d'arrivée.
// Rendre le texte de la révision déplacée en jaune avec un double barré
// et doublement souligné en bleu à la révision déplacée.
revisionOptions.MovedFromTextColor = RevisionColor.Yellow;
revisionOptions.MovedFromTextEffect = RevisionTextEffect.DoubleStrikeThrough;
revisionOptions.MovedToTextColor = RevisionColor.ClassicBlue;
revisionOptions.MovedToTextEffect = RevisionTextEffect.DoubleUnderline;

// Rendre les révisions de format en rouge foncé et en gras.
revisionOptions.RevisedPropertiesColor = RevisionColor.DarkRed;
revisionOptions.RevisedPropertiesEffect = RevisionTextEffect.Bold;

// Placez une barre bleu foncé épaisse sur le côté gauche de la page à côté des lignes affectées par les révisions.
revisionOptions.RevisionBarsColor = RevisionColor.DarkBlue;
revisionOptions.RevisionBarsWidth = 15.0f;

// Afficher les marques de révision et le texte original.
revisionOptions.ShowOriginalRevision = true;
revisionOptions.ShowRevisionMarks = true;

// Faites en sorte que les mouvements, les suppressions, les révisions de formatage et les commentaires s'affichent dans des bulles vertes
// sur le côté droit de la page.
revisionOptions.ShowInBalloons = ShowInBalloons.Format;
revisionOptions.CommentColor = RevisionColor.BrightGreen;

// Ces fonctionnalités ne s'appliquent qu'aux formats tels que .pdf ou .jpg.
doc.Save(ArtifactsDir + "Revision.RevisionOptions.pdf");
```

### Voir également

* enum [RevisionTextEffect](../../revisiontexteffect/)
* class [RevisionOptions](../)
* espace de noms [Aspose.Words.Layout](../../../aspose.words.layout/)
* Assemblée [Aspose.Words](../../../)
