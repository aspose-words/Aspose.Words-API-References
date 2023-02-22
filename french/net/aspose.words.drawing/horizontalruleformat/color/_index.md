---
title: HorizontalRuleFormat.Color
second_title: Référence de l'API Aspose.Words pour .NET
description: HorizontalRuleFormat propriété. Obtient ou définit la couleur du pinceau qui remplit la règle horizontale.
type: docs
weight: 20
url: /fr/net/aspose.words.drawing/horizontalruleformat/color/
---
## HorizontalRuleFormat.Color property

Obtient ou définit la couleur du pinceau qui remplit la règle horizontale.

```csharp
public Color Color { get; set; }
```

### Remarques

Il s'agit d'un raccourci vers leColor propriété.

La valeur par défaut est Gray.

### Exemples

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
* espace de noms [Aspose.Words.Drawing](../../horizontalruleformat/)
* Assemblée [Aspose.Words](../../../)


