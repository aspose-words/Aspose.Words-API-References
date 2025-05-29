---
title: RevisionOptions.ShowRevisionBars
linktitle: ShowRevisionBars
articleTitle: ShowRevisionBars
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété ShowRevisionBars de RevisionOptions améliore la clarté du document en affichant des barres de révision pour le contenu modifié. Valeur par défaut : true.
type: docs
weight: 200
url: /fr/net/aspose.words.layout/revisionoptions/showrevisionbars/
---
## RevisionOptions.ShowRevisionBars property

Permet de spécifier si les barres de révision doivent être rendues à proximité des lignes contenant du contenu révisé. La valeur par défaut est`vrai` .

```csharp
public bool ShowRevisionBars { get; set; }
```

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

* class [RevisionOptions](../)
* espace de noms [Aspose.Words.Layout](../../../aspose.words.layout/)
* Assemblée [Aspose.Words](../../../)
