---
title: RevisionTextEffect Enum
linktitle: RevisionTextEffect
articleTitle: RevisionTextEffect
second_title: Aspose.Words pour .NET
description: Aspose.Words.Layout.RevisionTextEffect énumération. Permet de spécifier leffet de décoration pour les révisions du texte du document en C#.
type: docs
weight: 3400
url: /fr/net/aspose.words.layout/revisiontexteffect/
---
## RevisionTextEffect enumeration

Permet de spécifier l'effet de décoration pour les révisions du texte du document.

```csharp
public enum RevisionTextEffect
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| None | `0` | Le contenu révisé n'a aucun effet spécial appliqué. Cela correspond àNoHighlight . |
| Color | `1` | Le contenu révisé est mis en évidence uniquement en couleur. |
| Bold | `2` | Le contenu révisé est mis en gras et en couleur. |
| Italic | `3` | Le contenu révisé est en italique et en couleur. |
| Underline | `4` | Le contenu révisé est souligné et coloré. |
| DoubleUnderline | `5` | Le contenu révisé est souligné deux fois et coloré. |
| StrikeThrough | `6` | Le contenu révisé est barré et coloré. |
| DoubleStrikeThrough | `7` | Le contenu révisé est doublement souligné et coloré. |
| Hidden | `8` | Le contenu révisé est masqué. |

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
