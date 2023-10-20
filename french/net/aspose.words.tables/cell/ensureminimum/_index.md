---
title: Cell.EnsureMinimum
linktitle: EnsureMinimum
articleTitle: EnsureMinimum
second_title: Aspose.Words pour .NET
description: Cell EnsureMinimum méthode. Si le dernier enfant nest pas un paragraphe crée et ajoute un paragraphe vide en C#.
type: docs
weight: 140
url: /fr/net/aspose.words.tables/cell/ensureminimum/
---
## Cell.EnsureMinimum method

Si le dernier enfant n'est pas un paragraphe, crée et ajoute un paragraphe vide.

```csharp
public void EnsureMinimum()
```

## Exemples

Montre comment garantir qu'un nœud de cellule contient les nœuds dont nous avons besoin pour commencer à y ajouter du contenu.

```csharp
Document doc = new Document();
Table table = new Table(doc);
doc.FirstSection.Body.AppendChild(table);
Row row = new Row(doc);
table.AppendChild(row);
Cell cell = new Cell(doc);
row.AppendChild(cell);

// Les cellules peuvent contenir des paragraphes avec des éléments typiques tels que des tracés, des formes et même d'autres tableaux.
// Notre nouvelle cellule ne contient aucun paragraphe et nous ne pouvons pas y ajouter de contenu tel que des nœuds d'exécution et de forme jusqu'à ce qu'elle le fasse.
Assert.AreEqual(0, cell.GetChildNodes(NodeType.Any, true).Count);

// L'appel de la méthode "EnsureMinimum" sur une cellule garantira que
// la cellule contient au moins un paragraphe vide, auquel nous pouvons ensuite ajouter du contenu.
cell.EnsureMinimum();
cell.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));
```

### Voir également

* class [Cell](../)
* espace de noms [Aspose.Words.Tables](../../../aspose.words.tables/)
* Assemblée [Aspose.Words](../../../)
