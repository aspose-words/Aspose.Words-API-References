---
title: Class BorderCollection
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.BorderCollection classe. Une collection dobjets Border.
type: docs
weight: 80
url: /fr/net/aspose.words/bordercollection/
---
## BorderCollection class

Une collection d'objets Border.

```csharp
public sealed class BorderCollection : IEnumerable<Border>
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Bottom](../../aspose.words/bordercollection/bottom/) { get; } | Obtient la bordure inférieure. |
| [Color](../../aspose.words/bordercollection/color/) { get; set; } | Obtient ou définit la couleur de la bordure. |
| [Count](../../aspose.words/bordercollection/count/) { get; } | Obtient le nombre de bordures dans la collection. |
| [DistanceFromText](../../aspose.words/bordercollection/distancefromtext/) { get; set; } | Obtient ou définit la distance de la bordure à partir du texte en points. |
| [Horizontal](../../aspose.words/bordercollection/horizontal/) { get; } | Obtient la bordure horizontale utilisée entre les cellules ou les paragraphes conformes. |
| [Item](../../aspose.words/bordercollection/item/) { get; } | Récupère un objet Border par type de bordure. (2 indexers) |
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
| [Equals](../../aspose.words/bordercollection/equals/#equals)(BorderCollection) | Compare les collections de bordures. |
| [GetEnumerator](../../aspose.words/bordercollection/getenumerator/)() | Renvoie un objet énumérateur qui peut être utilisé pour parcourir toutes les bordures de la collection. |

### Remarques

Différents éléments de document ont des bordures différentes. Par exemple, ParagraphFormat a des bordures inférieure, gauche, droite et supérieure. Vous pouvez spécifier une mise en forme différente pour chaque bordure indépendamment ou énumérer toutes les bordures et appliquer la même mise en forme.

### Exemples

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

* class [Border](../border/)
* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)


