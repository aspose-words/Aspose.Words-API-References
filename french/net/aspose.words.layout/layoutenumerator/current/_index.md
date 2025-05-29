---
title: LayoutEnumerator.Current
linktitle: Current
articleTitle: Current
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Current de LayoutEnumerator pour accéder et modifier facilement la position actuelle dans votre modèle de mise en page pour une flexibilité de conception améliorée.
type: docs
weight: 20
url: /fr/net/aspose.words.layout/layoutenumerator/current/
---
## LayoutEnumerator.Current property

Obtient ou définit la position actuelle dans le modèle de mise en page. Cette propriété renvoie un objet opaque qui correspond à l'entité de mise en page actuelle.

```csharp
public object Current { get; set; }
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

* class [LayoutEnumerator](../)
* espace de noms [Aspose.Words.Layout](../../../aspose.words.layout/)
* Assemblée [Aspose.Words](../../../)
