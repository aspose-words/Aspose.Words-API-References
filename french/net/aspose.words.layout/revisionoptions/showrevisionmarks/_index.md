---
title: RevisionOptions.ShowRevisionMarks
linktitle: ShowRevisionMarks
articleTitle: ShowRevisionMarks
second_title: Aspose.Words pour .NET
description: Contrôlez la visibilité des révisions avec la propriété ShowRevisionMarks. Formatez facilement le texte de révision pour plus de clarté et améliorez la collaboration sur les documents. La valeur par défaut est « true ».
type: docs
weight: 210
url: /fr/net/aspose.words.layout/revisionoptions/showrevisionmarks/
---
## RevisionOptions.ShowRevisionMarks property

Permet de spécifier si le texte de révision doit être marqué avec un balisage de formatage spécial. La valeur par défaut est`vrai` .

```csharp
public bool ShowRevisionMarks { get; set; }
```

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

* class [RevisionOptions](../)
* espace de noms [Aspose.Words.Layout](../../../aspose.words.layout/)
* Assemblée [Aspose.Words](../../../)
