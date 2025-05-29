---
title: Table.EnsureMinimum
linktitle: EnsureMinimum
articleTitle: EnsureMinimum
second_title: Aspose.Words pour .NET
description: Découvrez la méthode Table EnsureMinimum, créez et ajoutez sans effort une ligne lorsque votre table est vide pour une gestion transparente des données.
type: docs
weight: 420
url: /fr/net/aspose.words.tables/table/ensureminimum/
---
## Table.EnsureMinimum method

Si la table ne contient aucune ligne, crée et ajoute une ligne[`Row`](../../row/) .

```csharp
public void EnsureMinimum()
```

## Exemples

Montre comment garantir qu'un nœud de table contient les nœuds dont nous avons besoin pour ajouter du contenu.

```csharp
Document doc = new Document();
Table table = new Table(doc);
doc.FirstSection.Body.AppendChild(table);

// Les tableaux contiennent des lignes, qui contiennent des cellules, qui peuvent contenir des paragraphes
// avec des éléments typiques tels que des exécutions, des formes et même d'autres tables.
// Notre nouvelle table n'a aucun de ces nœuds et nous ne pouvons pas y ajouter de contenu tant qu'elle n'en a pas.
Assert.AreEqual(0, table.GetChildNodes(NodeType.Any, true).Count);

// L'appel de la méthode « EnsureMinimum » sur une table garantira que
// le tableau comporte au moins une ligne et une cellule avec un paragraphe vide.
table.EnsureMinimum();
table.FirstRow.FirstCell.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));
```

### Voir également

* class [Table](../)
* espace de noms [Aspose.Words.Tables](../../../aspose.words.tables/)
* Assemblée [Aspose.Words](../../../)
