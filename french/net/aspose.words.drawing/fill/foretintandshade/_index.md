---
title: Fill.ForeTintAndShade
linktitle: ForeTintAndShade
articleTitle: ForeTintAndShade
second_title: Aspose.Words pour .NET
description: Ajustez la propriété ForeTintAndShade pour éclaircir ou assombrir facilement votre couleur de premier plan, améliorant ainsi votre conception avec précision et créativité.
type: docs
weight: 90
url: /fr/net/aspose.words.drawing/fill/foretintandshade/
---
## Fill.ForeTintAndShade property

Obtient ou définit une valeur double qui éclaircit ou assombrit la couleur de premier plan.

```csharp
public double ForeTintAndShade { get; set; }
```

### Exceptions

| exception | condition |
| --- | --- |
| ArgumentOutOfRangeException | Lancer si cette propriété est définie sur une valeur inférieure à -1 ou supérieure à 1. |

## Remarques

Les valeurs autorisées sont comprises entre -1 (la plus foncée) et 1 (la plus claire) pour cette propriété.

Zéro (0) est neutre.

## Exemples

Montre comment gérer l'éclaircissement et l'assombrissement de la couleur de police de premier plan.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

Fill textFill = doc.FirstSection.Body.FirstParagraph.Runs[0].Font.Fill;
textFill.ForeThemeColor = ThemeColor.Accent1;
if (textFill.ForeTintAndShade == 0)
    textFill.ForeTintAndShade = 0.5;

doc.Save(ArtifactsDir + "Shape.FillTintAndShade.docx");
```

### Voir également

* class [Fill](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
