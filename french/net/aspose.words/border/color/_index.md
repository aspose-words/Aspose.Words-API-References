---
title: Border.Color
linktitle: Color
articleTitle: Color
second_title: Aspose.Words pour .NET
description: Personnalisez vos créations sans effort avec la propriété Couleur de bordure, vous permettant de définir et de modifier les couleurs de bordure pour un impact visuel époustouflant.
type: docs
weight: 10
url: /fr/net/aspose.words/border/color/
---
## Border.Color property

Obtient ou définit la couleur de la bordure.

```csharp
public Color Color { get; set; }
```

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
