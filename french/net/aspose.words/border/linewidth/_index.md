---
title: Border.LineWidth
second_title: Référence de l'API Aspose.Words pour .NET
description: Border propriété. Obtient ou définit la largeur de la bordure en points.
type: docs
weight: 50
url: /fr/net/aspose.words/border/linewidth/
---
## Border.LineWidth property

Obtient ou définit la largeur de la bordure en points.

```csharp
public double LineWidth { get; set; }
```

### Remarques

Si vous définissez une largeur de ligne supérieure à zéro alors que le style de ligne est aucun, le style de ligne is est automatiquement remplacé par une seule ligne.

### Exemples

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
* espace de noms [Aspose.Words](../../border/)
* Assemblée [Aspose.Words](../../../)


