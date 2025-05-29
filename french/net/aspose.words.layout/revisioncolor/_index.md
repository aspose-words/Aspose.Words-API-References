---
title: RevisionColor Enum
linktitle: RevisionColor
articleTitle: RevisionColor
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.Layout.RevisionColor pour personnaliser les couleurs de révision des documents, améliorant ainsi la clarté et la collaboration dans vos documents.
type: docs
weight: 3830
url: /fr/net/aspose.words.layout/revisioncolor/
---
## RevisionColor enumeration

Permet de spécifier la couleur des révisions du document.

```csharp
public enum RevisionColor
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Auto | `0` | Par défaut. |
| Black | `1` | Représente la couleur 000000. |
| Blue | `2` | Représente la couleur 2e97d3. |
| BrightGreen | `3` | Représente la couleur 84a35b. |
| ClassicBlue | `4` | Représente la couleur 0000ff. |
| ClassicRed | `5` | Représente la couleur ff0000. |
| DarkBlue | `6` | Représente la couleur 376e96. |
| DarkRed | `7` | Représente 881824 couleurs. |
| DarkYellow | `8` | Représente la couleur e09a2b. |
| Gray25 | `9` | Représente la couleur a0a3a9. |
| Gray50 | `10` | Représente la couleur 50565e. |
| Green | `11` | Représente la couleur 2c6234. |
| Pink | `12` | Représente la couleur ce338f. |
| Red | `13` | Représente la couleur b5082e. |
| Teal | `14` | Représente la couleur 1b9cab. |
| Turquoise | `15` | Représente la couleur 3eafc2. |
| Violet | `16` | Représente 633277 couleurs. |
| White | `17` | Représente la couleur ffffff. |
| Yellow | `18` | Représente la couleur fad272. |
| LightPink | `19` | Représente la couleur fce6f4. |
| LightBlue | `20` | Représente la couleur e1f2fa. |
| LightYellow | `21` | Représente la couleur fef4de. |
| LightPurple | `22` | Représente la couleur de la tête. |
| LightOrange | `23` | Représente la couleur fce3d0. |
| LightGreen | `24` | Représente la couleur e9f8ce. |
| Gray | `25` | Représente la couleur définie. |
| NoHighlight | `26` | Aucune couleur n'est utilisée pour mettre en évidence les modifications de révision. |
| ByAuthor | `27` | Les révisions de chaque auteur reçoivent leur propre couleur de surbrillance à partir d'un ensemble prédéfini de couleurs à contraste élevé. |

## Exemples

Montre comment modifier l’apparence des révisions dans un document de sortie rendu.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérez une révision, puis changez la couleur de toutes les révisions en vert.
builder.Writeln("This is not a revision.");
doc.StartTrackRevisions("John Doe", DateTime.Now);
builder.Writeln("This is a revision.");
doc.StopTrackRevisions();
builder.Writeln("This is not a revision.");

// Supprimez la barre qui apparaît à gauche de chaque ligne révisée.
doc.LayoutOptions.RevisionOptions.InsertedTextColor = RevisionColor.BrightGreen;
doc.LayoutOptions.RevisionOptions.ShowRevisionBars = false;
doc.LayoutOptions.RevisionOptions.RevisionBarsPosition = HorizontalAlignment.Right;

doc.Save(ArtifactsDir + "Revision.LayoutOptionsRevisions.pdf");
```

### Voir également

* espace de noms [Aspose.Words.Layout](../../aspose.words.layout/)
* Assemblée [Aspose.Words](../../)
