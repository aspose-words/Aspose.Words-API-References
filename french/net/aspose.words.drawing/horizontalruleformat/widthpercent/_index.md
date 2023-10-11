---
title: HorizontalRuleFormat.WidthPercent
second_title: Référence de l'API Aspose.Words pour .NET
description: HorizontalRuleFormat propriété. Obtient ou définit la longueur de la règle horizontale spécifiée exprimée en pourcentage de la largeur de la fenêtre.
type: docs
weight: 50
url: /fr/net/aspose.words.drawing/horizontalruleformat/widthpercent/
---
## HorizontalRuleFormat.WidthPercent property

Obtient ou définit la longueur de la règle horizontale spécifiée exprimée en pourcentage de la largeur de la fenêtre.

```csharp
public double WidthPercent { get; set; }
```

### Exceptions

| exception | condition |
| --- | --- |
| ArgumentOutOfRangeException | Lance lorsque l'argument est hors de la plage des valeurs valides. |

### Remarques

Les valeurs valides vont de 1 à 100 inclus.

La valeur par défaut est 100.

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


