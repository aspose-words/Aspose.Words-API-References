---
title: HorizontalRuleFormat.Height
linktitle: Height
articleTitle: Height
second_title: Aspose.Words pour .NET
description: Ajustez facilement la hauteur de votre règle horizontale. Explorez la propriété « Hauteur » pour personnaliser le design de vos projets web. Améliorez votre mise en page dès aujourd'hui !
type: docs
weight: 30
url: /fr/net/aspose.words.drawing/horizontalruleformat/height/
---
## HorizontalRuleFormat.Height property

Obtient ou définit la hauteur de la règle horizontale.

```csharp
public double Height { get; set; }
```

### Exceptions

| exception | condition |
| --- | --- |
| ArgumentOutOfRangeException | Lancé lorsque l'argument est hors de la plage de valeurs valides. |

## Remarques

Il s'agit d'un raccourci vers le[`Height`](../../shapebase/height/) propriété.

Les valeurs valides vont de 0 à 1584 inclus.

La valeur par défaut est 1,5.

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
