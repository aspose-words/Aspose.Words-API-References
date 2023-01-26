---
title: LayoutCollector
second_title: Référence de l'API Aspose.Words pour .NET
description: Cette classe permet de calculer les numéros de page des nœuds de document.
type: docs
weight: 3120
url: /fr/net/aspose.words.layout/layoutcollector/
---
## LayoutCollector class

Cette classe permet de calculer les numéros de page des nœuds de document.

```csharp
public class LayoutCollector
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [LayoutCollector](layoutcollector/)(Document) | Initialise une instance de cette classe. |

## Propriétés

| Nom | La description |
| --- | --- |
| [Document](../../aspose.words.layout/layoutcollector/document/) { get; set; } | Obtient ou définit le document auquel cette instance de collecteur est attachée. |

## Méthodes

| Nom | La description |
| --- | --- |
| [Clear](../../aspose.words.layout/layoutcollector/clear/)() | Efface toutes les données de mise en page collectées. Appelez cette méthode après la mise à jour manuelle du document ou la reconstruction de la mise en page. |
| [GetEndPageIndex](../../aspose.words.layout/layoutcollector/getendpageindex/)(Node) | Obtient l'index de base 1 de la page où se termine le nœud. Renvoie 0 si le nœud ne peut pas être mappé sur une page. |
| [GetEntity](../../aspose.words.layout/layoutcollector/getentity/)(Node) | Renvoie une position opaque du[`LayoutEnumerator`](../layoutenumerator/) qui correspond au nœud spécifié. Vous pouvez utiliser la valeur renvoyée comme argument pour[`Current`](../layoutenumerator/current/) étant donné que le document étant énuméré et le document du nœud sont les mêmes. |
| [GetNumPagesSpanned](../../aspose.words.layout/layoutcollector/getnumpagesspanned/)(Node) | Obtient le nombre de pages que le nœud spécifié s'étend. 0 si le nœud se trouve dans une seule page. C'est la même chose que[`GetEndPageIndex`](./getendpageindex/) -[`GetStartPageIndex`](./getstartpageindex/) . |
| [GetStartPageIndex](../../aspose.words.layout/layoutcollector/getstartpageindex/)(Node) | Obtient l'index de base 1 de la page où commence le nœud. Renvoie 0 si le nœud ne peut pas être mappé sur une page. |

### Remarques

Lorsque vous créez un`LayoutCollector` et indiquez un[`Document`](../../aspose.words/document/)objet de document auquel s'attacher, le collecteur enregistrera le mappage des nœuds de document aux objets de mise en page lorsque le document est formaté en pages.

Vous pourrez savoir sur quelle page se trouve un nœud de document particulier (par exemple, passage, paragraphe ou cellule de tableau) en utilisant la[`GetStartPageIndex`](./getstartpageindex/) ,[`GetEndPageIndex`](./getendpageindex/) et[`GetNumPagesSpanned`](./getnumpagesspanned/) méthodes. Ces méthodes créent automatiquement le modèle de mise en page du document et mettent à jour les champs si nécessaire.

Lorsque vous n'avez plus besoin de collecter des informations de mise en page, il est préférable de définir le[`Document`](./document/) propriété à null pour éviter la collecte inutile de mappages de mise en page supplémentaires.

### Exemples

Montre comment voir les plages de pages couvertes par un nœud.

```csharp
Document doc = new Document();
LayoutCollector layoutCollector = new LayoutCollector(doc);

// Appelez la méthode "GetNumPagesSpanned" pour compter le nombre de pages sur lesquelles s'étend le contenu de notre document.
// Puisque le document est vide, ce nombre de pages est actuellement nul.
Assert.AreEqual(doc, layoutCollector.Document);
Assert.AreEqual(0, layoutCollector.GetNumPagesSpanned(doc));

// Remplir le document avec 5 pages de contenu.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Section 1");
builder.InsertBreak(BreakType.PageBreak);
builder.InsertBreak(BreakType.PageBreak);
builder.InsertBreak(BreakType.SectionBreakEvenPage);
builder.Write("Section 2");
builder.InsertBreak(BreakType.PageBreak);
builder.InsertBreak(BreakType.PageBreak);

// Avant le collecteur de disposition, nous devons appeler la méthode "UpdatePageLayout" pour nous donner
// un chiffre précis pour toute métrique liée à la mise en page, telle que le nombre de pages.
Assert.AreEqual(0, layoutCollector.GetNumPagesSpanned(doc));

layoutCollector.Clear();
doc.UpdatePageLayout();

Assert.AreEqual(5, layoutCollector.GetNumPagesSpanned(doc));

// Nous pouvons voir les numéros des pages de début et de fin de n'importe quel nœud et leurs étendues de page globales.
NodeCollection nodes = doc.GetChildNodes(NodeType.Any, true);
foreach (Node node in nodes)
{
    Console.WriteLine($"->  NodeType.{node.NodeType}: ");
    Console.WriteLine(
        $"\tStarts on page {layoutCollector.GetStartPageIndex(node)}, ends on page {layoutCollector.GetEndPageIndex(node)}," +
        $" spanning {layoutCollector.GetNumPagesSpanned(node)} pages.");
}

// Nous pouvons parcourir les entités de mise en page à l'aide d'un LayoutEnumerator.
LayoutEnumerator layoutEnumerator = new LayoutEnumerator(doc);

Assert.AreEqual(LayoutEntityType.Page, layoutEnumerator.Type);

// Le LayoutEnumerator peut traverser la collection d'entités de mise en page comme un arbre.
// Nous pouvons également l'appliquer à l'entité de mise en page correspondante de n'importe quel nœud.
layoutEnumerator.Current = layoutCollector.GetEntity(doc.GetChild(NodeType.Paragraph, 1, true));

Assert.AreEqual(LayoutEntityType.Span, layoutEnumerator.Type);
Assert.AreEqual("¶", layoutEnumerator.Text);
```

### Voir également

* espace de noms [Aspose.Words.Layout](../../aspose.words.layout/)
* Assemblée [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
