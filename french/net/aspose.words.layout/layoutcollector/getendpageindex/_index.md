---
title: LayoutCollector.GetEndPageIndex
linktitle: GetEndPageIndex
articleTitle: GetEndPageIndex
second_title: Aspose.Words pour .NET
description: Découvrez la méthode GetEndPageIndex de LayoutCollector pour trouver facilement l'index de base 1 de la page de fin d'un nœud. Simplifiez le mappage de vos pages dès aujourd'hui !
type: docs
weight: 40
url: /fr/net/aspose.words.layout/layoutcollector/getendpageindex/
---
## LayoutCollector.GetEndPageIndex method

Obtient l'index de base 1 de la page où se termine le nœud. Renvoie 0 si le nœud ne peut être mappé à une page.

```csharp
public int GetEndPageIndex(Node node)
```

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
