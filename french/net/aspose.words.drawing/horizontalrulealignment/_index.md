---
title: HorizontalRuleAlignment Enum
linktitle: HorizontalRuleAlignment
articleTitle: HorizontalRuleAlignment
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.HorizontalRuleAlignment pour un contrôle précis de l'alignement des règles horizontales, améliorant ainsi la mise en forme et la conception de votre document.
type: docs
weight: 1370
url: /fr/net/aspose.words.drawing/horizontalrulealignment/
---
## HorizontalRuleAlignment enumeration

Représente l'alignement de la règle horizontale spécifiée.

```csharp
public enum HorizontalRuleAlignment
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Left | `0` | Aligné à gauche. |
| Center | `1` | Aligné au centre. |
| Right | `2` | Aligné à droite. |

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

* espace de noms [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../)
