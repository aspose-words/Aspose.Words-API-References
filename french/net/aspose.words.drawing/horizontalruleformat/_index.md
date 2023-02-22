---
title: Class HorizontalRuleFormat
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Drawing.HorizontalRuleFormat classe. Représente le formatage de la règle horizontale.
type: docs
weight: 920
url: /fr/net/aspose.words.drawing/horizontalruleformat/
---
## HorizontalRuleFormat class

Représente le formatage de la règle horizontale.

```csharp
public class HorizontalRuleFormat
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Alignment](../../aspose.words.drawing/horizontalruleformat/alignment/) { get; set; } | Obtient ou définit l'alignement de la règle horizontale. |
| [Color](../../aspose.words.drawing/horizontalruleformat/color/) { get; set; } | Obtient ou définit la couleur du pinceau qui remplit la règle horizontale. |
| [Height](../../aspose.words.drawing/horizontalruleformat/height/) { get; set; } | Obtient ou définit la hauteur de la règle horizontale. |
| [NoShade](../../aspose.words.drawing/horizontalruleformat/noshade/) { get; set; } | Indique la présence d'un ombrage 3D pour la règle horizontale. Si vrai, alors la règle horizontale est sans ombrage 3D et une couleur unie est utilisée. |
| [WidthPercent](../../aspose.words.drawing/horizontalruleformat/widthpercent/) { get; set; } | Obtient ou définit la longueur de la règle horizontale spécifiée exprimée en pourcentage de la largeur de la fenêtre. |

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

* espace de noms [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../)


