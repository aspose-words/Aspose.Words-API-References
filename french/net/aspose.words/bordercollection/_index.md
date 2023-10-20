---
title: BorderCollection Class
linktitle: BorderCollection
articleTitle: BorderCollection
second_title: Aspose.Words pour .NET
description: Aspose.Words.BorderCollection classe. Une collection deBorder objets en C#.
type: docs
weight: 90
url: /fr/net/aspose.words/bordercollection/
---
## BorderCollection class

Une collection de[`Border`](../border/) objets.

Pour en savoir plus, visitez le[Programmation avec des documents](https://docs.aspose.com/words/net/programming-with-documents/) article documentaire.

```csharp
public sealed class BorderCollection : IEnumerable<Border>
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Bottom](../../aspose.words/bordercollection/bottom/) { get; } | Obtient la bordure inférieure. |
| [Color](../../aspose.words/bordercollection/color/) { get; set; } | Obtient ou définit la couleur de la bordure. |
| [Count](../../aspose.words/bordercollection/count/) { get; } | Obtient le nombre de bordures dans la collection. |
| [DistanceFromText](../../aspose.words/bordercollection/distancefromtext/) { get; set; } | Obtient ou définit la distance entre la bordure et le texte en points. |
| [Horizontal](../../aspose.words/bordercollection/horizontal/) { get; } | Obtient la bordure horizontale utilisée entre les cellules ou les paragraphes conformes. |
| [Item](../../aspose.words/bordercollection/item/) { get; } | Récupère un[`Border`](../border/) objet par type de bordure. (2 indexers) |
| [Left](../../aspose.words/bordercollection/left/) { get; } | Obtient la bordure gauche. |
| [LineStyle](../../aspose.words/bordercollection/linestyle/) { get; set; } | Obtient ou définit le style de bordure. |
| [LineWidth](../../aspose.words/bordercollection/linewidth/) { get; set; } | Obtient ou définit la largeur de la bordure en points. |
| [Right](../../aspose.words/bordercollection/right/) { get; } | Obtient la bordure droite. |
| [Shadow](../../aspose.words/bordercollection/shadow/) { get; set; } | Obtient ou définit une valeur indiquant si la bordure a une ombre. |
| [Top](../../aspose.words/bordercollection/top/) { get; } | Obtient la bordure supérieure. |
| [Vertical](../../aspose.words/bordercollection/vertical/) { get; } | Obtient la bordure verticale utilisée entre les cellules. |

## Méthodes

| Nom | La description |
| --- | --- |
| [ClearFormatting](../../aspose.words/bordercollection/clearformatting/)() | Supprime toutes les bordures d'un objet. |
| [Equals](../../aspose.words/bordercollection/equals/#equals)(*BorderCollection*) | Compare les collections de bordures. |
| [GetEnumerator](../../aspose.words/bordercollection/getenumerator/)() | Renvoie un objet énumérateur qui peut être utilisé pour parcourir toutes les bordures de la collection. |

## Remarques

Différents éléments du document ont des bordures différentes. Par exemple,[`ParagraphFormat`](../paragraphformat/)a[`Bottom`](./bottom/) ,[`Left`](./left/) ,[`Right`](./right/) et[`Top`](./top/) borders. Vous pouvez spécifier un formatage différent pour chaque bordure indépendamment ou énumérer toutes les bordures et appliquer le même formatage.

## Exemples

Montre comment insérer un paragraphe avec une bordure supérieure.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Border topBorder = builder.ParagraphFormat.Borders.Top;
topBorder.LineWidth = 4.0d;
topBorder.LineStyle = LineStyle.DashSmallGap;
// Définit ThemeColor uniquement lorsque LineWidth ou LineStyle est défini.
topBorder.ThemeColor = ThemeColor.Accent1;
topBorder.TintAndShade = 0.25d;

builder.Writeln("Text with a top border.");

doc.Save(ArtifactsDir + "Border.ParagraphTopBorder.docx");
```

### Voir également

* class [Border](../border/)
* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
