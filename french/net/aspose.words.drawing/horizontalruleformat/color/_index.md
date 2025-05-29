---
title: HorizontalRuleFormat.Color
linktitle: Color
articleTitle: Color
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Couleur HorizontalRuleFormat pour personnaliser votre design. Définissez ou obtenez facilement la couleur du pinceau pour un effet de règle horizontale époustouflant !
type: docs
weight: 20
url: /fr/net/aspose.words.drawing/horizontalruleformat/color/
---
## HorizontalRuleFormat.Color property

Obtient ou définit la couleur du pinceau qui remplit la règle horizontale.

```csharp
public Color Color { get; set; }
```

## Remarques

Il s'agit d'un raccourci vers le[`Color`](../../fill/color/) propriété.

La valeur par défaut est Gray .

## Exemples

Montre comment insérer une forme de règle horizontale et personnaliser sa mise en forme.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Shape shape = builder.InsertHorizontalRule();

HorizontalRuleFormat horizontalRuleFormat = shape.HorizontalRuleFormat;
horizontalRuleFormat.Alignment = HorizontalRuleAlignment.Center;
horizontalRuleFormat.WidthPercent = 70;
horizontalRuleFormat.Height = 3;
horizontalRuleFormat.Color = Color.Blue;
horizontalRuleFormat.NoShade = true;

Assert.True(shape.IsHorizontalRule);
Assert.True(shape.HorizontalRuleFormat.NoShade);
```

### Voir également

* class [HorizontalRuleFormat](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
