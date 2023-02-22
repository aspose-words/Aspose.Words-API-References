---
title: Class Border
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Border classe. Représente une bordure dun objet.
type: docs
weight: 70
url: /fr/net/aspose.words/border/
---
## Border class

Représente une bordure d'un objet.

```csharp
public class Border : InternableComplexAttr
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Color](../../aspose.words/border/color/) { get; set; } | Obtient ou définit la couleur de la bordure. |
| [DistanceFromText](../../aspose.words/border/distancefromtext/) { get; set; } | Obtient ou définit la distance de la bordure à partir du texte ou du bord de la page en points. |
| [IsVisible](../../aspose.words/border/isvisible/) { get; } | Renvoie vrai si le LineStyle n'est pas LineStyle.None. |
| [LineStyle](../../aspose.words/border/linestyle/) { get; set; } | Obtient ou définit le style de bordure. |
| [LineWidth](../../aspose.words/border/linewidth/) { get; set; } | Obtient ou définit la largeur de la bordure en points. |
| [Shadow](../../aspose.words/border/shadow/) { get; set; } | Obtient ou définit une valeur indiquant si la bordure a une ombre. |

## Méthodes

| Nom | La description |
| --- | --- |
| [ClearFormatting](../../aspose.words/border/clearformatting/)() | Réinitialise les propriétés de bordure aux valeurs par défaut. |
| [Equals](../../aspose.words/border/equals/#equals)(Border) | Détermine si la bordure spécifiée est égale en valeur à la bordure actuelle. |
| override [Equals](../../aspose.words/border/equals/#equals_1)(object) | Détermine si l'objet spécifié est égal en valeur à l'objet actuel. |
| override [GetHashCode](../../aspose.words/border/gethashcode/)() | Sert de fonction de hachage pour ce type. |

### Remarques

Les bordures peuvent être appliquées à divers éléments de document, y compris le paragraphe, la suite de texte à l'intérieur d'un paragraphe ou d'une cellule de tableau.

### Exemples

Montre comment insérer une chaîne entourée d'une bordure dans un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Border.Color = Color.Green;
builder.Font.Border.LineWidth = 2.5d;
builder.Font.Border.LineStyle = LineStyle.DashDotStroker;

builder.Write("Text surrounded by green border.");

doc.Save(ArtifactsDir + "Border.FontBorder.docx");
```

Montre comment insérer un paragraphe avec une bordure supérieure.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Border topBorder = builder.ParagraphFormat.Borders[BorderType.Top];
topBorder.Color = Color.Red;
topBorder.LineWidth = 4.0d;
topBorder.LineStyle = LineStyle.DashSmallGap;

builder.Writeln("Text with a red top border.");

doc.Save(ArtifactsDir + "Border.ParagraphTopBorder.docx");
```

### Voir également

* class [InternableComplexAttr](../internablecomplexattr/)
* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)


