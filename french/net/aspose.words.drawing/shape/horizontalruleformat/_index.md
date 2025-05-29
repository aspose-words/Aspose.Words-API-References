---
title: Shape.HorizontalRuleFormat
linktitle: HorizontalRuleFormat
articleTitle: HorizontalRuleFormat
second_title: Aspose.Words pour .NET
description: Accédez aux propriétés HorizontalRuleFormat et personnalisez-les pour une plus grande flexibilité de conception. Optimisez vos formes avec des paramètres personnalisés pour des résultats uniques.
type: docs
weight: 110
url: /fr/net/aspose.words.drawing/shape/horizontalruleformat/
---
## Shape.HorizontalRuleFormat property

Donne accès aux propriétés de la forme de règle horizontale. Pour une forme qui n'est pas une règle horizontale, renvoie`nul` .

```csharp
public HorizontalRuleFormat HorizontalRuleFormat { get; }
```

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

* class [HorizontalRuleFormat](../../horizontalruleformat/)
* class [Shape](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
