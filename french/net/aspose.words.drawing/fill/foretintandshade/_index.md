---
title: Fill.ForeTintAndShade
linktitle: ForeTintAndShade
articleTitle: ForeTintAndShade
second_title: Aspose.Words pour .NET
description: Fill ForeTintAndShade propriété. Obtient ou définit une valeur double qui éclaircit ou assombrit la couleur de premier plan en C#.
type: docs
weight: 80
url: /fr/net/aspose.words.drawing/fill/foretintandshade/
---
## Fill.ForeTintAndShade property

Obtient ou définit une valeur double qui éclaircit ou assombrit la couleur de premier plan.

```csharp
public double ForeTintAndShade { get; set; }
```

## Remarques

Les valeurs autorisées sont comprises entre -1 (le plus sombre) et 1 (le plus clair) pour cette propriété. Zéro (0) est neutre. Tenter de définir cette propriété sur une valeur inférieure à -1 ou supérieure à 1 entraîneArgumentOutOfRangeException.

## Exemples

Montre comment gérer l’éclaircissement et l’assombrissement de la couleur de la police de premier plan.

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
