---
title: RevisionOptions.RevisionBarsPosition
linktitle: RevisionBarsPosition
articleTitle: RevisionBarsPosition
second_title: Aspose.Words pour .NET
description: Découvrez comment personnaliser la propriété RevisionBarsPosition dans RevisionOptions pour améliorer l'apparence de votre document. La valeur par défaut est « Extérieur ».
type: docs
weight: 160
url: /fr/net/aspose.words.layout/revisionoptions/revisionbarsposition/
---
## RevisionOptions.RevisionBarsPosition property

Obtient ou définit la position de rendu des barres de révision. La valeur par défaut estOutside .

```csharp
public HorizontalAlignment RevisionBarsPosition { get; set; }
```

### Exceptions

| exception | condition |
| --- | --- |
| ArgumentOutOfRangeException | Valeurs deCenter etInside ne sont pas autorisés. |

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

* enum [HorizontalAlignment](../../../aspose.words.drawing/horizontalalignment/)
* class [RevisionOptions](../)
* espace de noms [Aspose.Words.Layout](../../../aspose.words.layout/)
* Assemblée [Aspose.Words](../../../)
