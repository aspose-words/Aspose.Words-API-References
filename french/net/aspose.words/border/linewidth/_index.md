---
title: Border.LineWidth
linktitle: LineWidth
articleTitle: LineWidth
second_title: Aspose.Words pour .NET
description: Border LineWidth propriété. Obtient ou définit la largeur de la bordure en points en C#.
type: docs
weight: 50
url: /fr/net/aspose.words/border/linewidth/
---
## Border.LineWidth property

Obtient ou définit la largeur de la bordure en points.

```csharp
public double LineWidth { get; set; }
```

## Remarques

Si vous définissez une largeur de ligne supérieure à zéro alors que le style de ligne est aucun, le style de ligne is est automatiquement remplacé par une seule ligne.

## Exemples

Montre comment insérer une chaîne entourée d'une bordure dans un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Border.Color = Color.Green;
builder.Font.Border.LineWidth = 2.5d;
builder.Font.Border.LineStyle = LineStyle.DashDotStroker;

builder.Write("Text surrounded by green border.");

doc.Save(ArtifactsDir + "Border.FontBorder.docx");
```

### Voir également

* class [Border](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
