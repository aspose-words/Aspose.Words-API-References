---
title: Border.LineWidth
linktitle: LineWidth
articleTitle: LineWidth
second_title: Aspose.Words pour .NET
description: Ajustez la propriété Border LineWidth pour personnaliser l'épaisseur de la bordure en points, améliorant ainsi la précision et l'attrait visuel de votre conception.
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

Si vous définissez une largeur de ligne supérieure à zéro lorsque le style de ligne est aucun, le style de ligne is est automatiquement modifié en ligne unique.

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
