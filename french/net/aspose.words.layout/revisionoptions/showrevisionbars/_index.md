---
title: RevisionOptions.ShowRevisionBars
second_title: Référence de l'API Aspose.Words pour .NET
description: RevisionOptions propriété. Permet de spécifier si les barres de révision doivent être rendues près des lignes contenant du contenu révisé. La valeur par défaut estvrai .
type: docs
weight: 180
url: /fr/net/aspose.words.layout/revisionoptions/showrevisionbars/
---
## RevisionOptions.ShowRevisionBars property

Permet de spécifier si les barres de révision doivent être rendues près des lignes contenant du contenu révisé. La valeur par défaut est`vrai` .

```csharp
public bool ShowRevisionBars { get; set; }
```

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

* class [RevisionOptions](../)
* espace de noms [Aspose.Words.Layout](../../revisionoptions/)
* Assemblée [Aspose.Words](../../../)


