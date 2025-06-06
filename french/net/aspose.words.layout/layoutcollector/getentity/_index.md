---
title: LayoutCollector.GetEntity
linktitle: GetEntity
articleTitle: GetEntity
second_title: Aspose.Words pour .NET
description: Découvrez la méthode GetEntity de LayoutCollector, récupérez sans effort la position du LayoutEnumerator pour une navigation transparente dans les documents et une productivité améliorée.
type: docs
weight: 50
url: /fr/net/aspose.words.layout/layoutcollector/getentity/
---
## LayoutCollector.GetEntity method

Renvoie une position opaque du[`LayoutEnumerator`](../../layoutenumerator/) qui correspond au nœud spécifié. Vous pouvez utiliser la valeur renvoyée comme argument pour[`Current`](../../layoutenumerator/current/) étant donné que le document étant énuméré et le document du nœud sont les mêmes.

```csharp
public object GetEntity(Node node)
```

## Remarques

Cette méthode fonctionne uniquement pour[`Paragraph`](../../../aspose.words/paragraph/) nœuds, ainsi que les nœuds en ligne indivisibles, par exemple[`BookmarkStart`](../../../aspose.words/bookmarkstart/) ou[`Shape`](../../../aspose.words.drawing/shape/) . Cela ne fonctionne pas pour[`Run`](../../../aspose.words/run/) ,[`Cell`](../../../aspose.words.tables/cell/)[`Row`](../../../aspose.words.tables/row/) ou[`Table`](../../../aspose.words.tables/table/) nœuds et nœuds dans l'en-tête/pied de page.

Notez que l'entité est revenue pour un[`Paragraph`](../../../aspose.words/paragraph/)Le nœud est une section de saut de paragraphe. Utilisez la méthode appropriée pour remonter à la ligne parente.

Si vous avez besoin de naviguer vers un[`Run`](../../../aspose.words/run/) de texte, vous pouvez alors insérer un signet juste avant it , puis naviguer vers le signet à la place.

Si vous avez besoin de naviguer vers un[`Cell`](../../../aspose.words.tables/cell/) nœud, vous pouvez alors passer à un[`Paragraph`](../../../aspose.words/paragraph/) dans cette cellule, puis remonter jusqu'à une entité parente. La même approche peut être utilisée pour[`Row`](../../../aspose.words.tables/row/) et[`Table`](../../../aspose.words.tables/table/) nœuds.

## Exemples

Montre comment voir les plages de pages qu'un nœud couvre.

```csharp
Document doc = new Document();
LayoutCollector layoutCollector = new LayoutCollector(doc);

// Appelez la méthode « GetNumPagesSpanned » pour compter le nombre de pages sur lesquelles s'étend le contenu de notre document.
// Étant donné que le document est vide, ce nombre de pages est actuellement nul.
Assert.AreEqual(doc, layoutCollector.Document);
Assert.AreEqual(0, layoutCollector.GetNumPagesSpanned(doc));

// Remplissez le document avec 5 pages de contenu.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Section 1");
builder.InsertBreak(BreakType.PageBreak);
builder.InsertBreak(BreakType.PageBreak);
builder.InsertBreak(BreakType.SectionBreakEvenPage);
builder.Write("Section 2");
builder.InsertBreak(BreakType.PageBreak);
builder.InsertBreak(BreakType.PageBreak);

// Avant le collecteur de mise en page, nous devons appeler la méthode "UpdatePageLayout" pour nous donner
// un chiffre précis pour toute mesure liée à la mise en page, telle que le nombre de pages.
Assert.AreEqual(0, layoutCollector.GetNumPagesSpanned(doc));

layoutCollector.Clear();
doc.UpdatePageLayout();

Assert.AreEqual(5, layoutCollector.GetNumPagesSpanned(doc));

// Nous pouvons voir les numéros des pages de début et de fin de n'importe quel nœud et leurs étendues de pages globales.
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

// Le LayoutEnumerator peut parcourir la collection d'entités de mise en page comme un arbre.
// Nous pouvons également l'appliquer à l'entité de mise en page correspondante de n'importe quel nœud.
layoutEnumerator.Current = layoutCollector.GetEntity(doc.GetChild(NodeType.Paragraph, 1, true));

Assert.AreEqual(LayoutEntityType.Span, layoutEnumerator.Type);
Assert.AreEqual("¶", layoutEnumerator.Text);
```

### Voir également

* class [Node](../../../aspose.words/node/)
* class [LayoutCollector](../)
* espace de noms [Aspose.Words.Layout](../../../aspose.words.layout/)
* Assemblée [Aspose.Words](../../../)
