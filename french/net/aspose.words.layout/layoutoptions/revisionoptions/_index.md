---
title: LayoutOptions.RevisionOptions
second_title: Référence de l'API Aspose.Words pour .NET
description: LayoutOptions propriété. Obtient les options de révision.
type: docs
weight: 70
url: /fr/net/aspose.words.layout/layoutoptions/revisionoptions/
---
## LayoutOptions.RevisionOptions property

Obtient les options de révision.

```csharp
public RevisionOptions RevisionOptions { get; }
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

* class [RevisionOptions](../../revisionoptions/)
* class [LayoutOptions](../)
* espace de noms [Aspose.Words.Layout](../../layoutoptions/)
* Assemblée [Aspose.Words](../../../)


