---
title: Table.EnsureMinimum
linktitle: EnsureMinimum
articleTitle: EnsureMinimum
second_title: Aspose.Words pour .NET
description: Table EnsureMinimum méthode. Si le tableau na pas de lignes en crée et en ajoute uneRow  en C#.
type: docs
weight: 400
url: /fr/net/aspose.words.tables/table/ensureminimum/
---
## Table.EnsureMinimum method

Si le tableau n'a pas de lignes, en crée et en ajoute une[`Row`](../../row/) .

```csharp
public void EnsureMinimum()
```

## Exemples

Montre comment garantir qu'un nœud de table contient les nœuds dont nous avons besoin pour ajouter du contenu.

```csharp
Document doc = new Document();
Table table = new Table(doc);
doc.FirstSection.Body.AppendChild(table);

// Les tableaux contiennent des lignes contenant des cellules pouvant contenir des paragraphes
// avec des éléments typiques tels que des courses, des formes et même d'autres tables.
// Notre nouvelle table n'a aucun de ces nœuds et nous ne pouvons pas y ajouter de contenu tant que ce n'est pas le cas.
Assert.AreEqual(0, table.GetChildNodes(NodeType.Any, true).Count);

// L'appel de la méthode "EnsureMinimum" sur une table garantira que
// le tableau comporte au moins une ligne et une cellule avec un paragraphe vide.
table.EnsureMinimum();
table.FirstRow.FirstCell.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));
```

### Voir également

* class [Table](../)
* espace de noms [Aspose.Words.Tables](../../../aspose.words.tables/)
* Assemblée [Aspose.Words](../../../)
