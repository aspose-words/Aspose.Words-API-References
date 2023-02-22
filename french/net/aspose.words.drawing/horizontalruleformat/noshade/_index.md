---
title: HorizontalRuleFormat.NoShade
second_title: Référence de l'API Aspose.Words pour .NET
description: HorizontalRuleFormat propriété. Indique la présence dun ombrage 3D pour la règle horizontale. Si vrai alors la règle horizontale est sans ombrage 3D et une couleur unie est utilisée.
type: docs
weight: 40
url: /fr/net/aspose.words.drawing/horizontalruleformat/noshade/
---
## HorizontalRuleFormat.NoShade property

Indique la présence d'un ombrage 3D pour la règle horizontale. Si vrai, alors la règle horizontale est sans ombrage 3D et une couleur unie est utilisée.

```csharp
public bool NoShade { get; set; }
```

### Remarques

La valeur par défaut est faux.

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


