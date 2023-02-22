---
title: Table.EnsureMinimum
second_title: Référence de l'API Aspose.Words pour .NET
description: Table méthode. Si le tableau na pas de lignes en crée et en ajoute une Ligne .
type: docs
weight: 400
url: /fr/net/aspose.words.tables/table/ensureminimum/
---
## Table.EnsureMinimum method

Si le tableau n'a pas de lignes, en crée et en ajoute une **Ligne** .

```csharp
public void EnsureMinimum()
```

### Exemples

Montre comment s'assurer qu'un nœud de table contient les nœuds dont nous avons besoin pour ajouter du contenu.

```csharp
Document doc = new Document();
Table table = new Table(doc);
doc.FirstSection.Body.AppendChild(table);

// Les tableaux contiennent des lignes, qui contiennent des cellules, qui peuvent contenir des paragraphes
// avec des éléments typiques tels que des suites, des formes et même d'autres tables.
// Notre nouvelle table n'a aucun de ces nœuds, et nous ne pouvons pas y ajouter de contenu tant qu'elle ne le fait pas.
Assert.AreEqual(0, table.GetChildNodes(NodeType.Any, true).Count);

// L'appel de la méthode "EnsureMinimum" sur une table garantira que
// le tableau a au moins une ligne et une cellule avec un paragraphe vide.
table.EnsureMinimum();
table.FirstRow.FirstCell.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));
```

### Voir également

* class [Table](../)
* espace de noms [Aspose.Words.Tables](../../table/)
* Assemblée [Aspose.Words](../../../)


