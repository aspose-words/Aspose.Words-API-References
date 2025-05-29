---
title: Row.EnsureMinimum
linktitle: EnsureMinimum
articleTitle: EnsureMinimum
second_title: Aspose.Words pour .NET
description: Découvrez la méthode Row EnsureMinimum, créez et ajoutez sans effort une cellule lorsqu'il n'en existe aucune, améliorant ainsi la gestion de votre structure de données.
type: docs
weight: 150
url: /fr/net/aspose.words.tables/row/ensureminimum/
---
## Row.EnsureMinimum method

Si le[`Row`](../) n'a pas de cellules, crée et ajoute une[`Cell`](../../cell/) .

```csharp
public void EnsureMinimum()
```

## Exemples

Montre comment garantir qu'un nœud de ligne contient les nœuds dont nous avons besoin pour commencer à y ajouter du contenu.

```csharp
Document doc = new Document();
Table table = new Table(doc);
doc.FirstSection.Body.AppendChild(table);
Row row = new Row(doc);
table.AppendChild(row);

// Les lignes contiennent des cellules, contenant des paragraphes avec des éléments typiques tels que des exécutions, des formes et même d'autres tableaux.
// Notre nouvelle ligne n'a aucun de ces nœuds et nous ne pouvons pas y ajouter de contenu tant qu'elle n'en a pas.
Assert.AreEqual(0, row.GetChildNodes(NodeType.Any, true).Count);

// L'appel de la méthode « EnsureMinimum » sur une table garantira que
// le tableau contient au moins une cellule avec un paragraphe vide.
row.EnsureMinimum();
row.FirstCell.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));
```

### Voir également

* class [Row](../)
* espace de noms [Aspose.Words.Tables](../../../aspose.words.tables/)
* Assemblée [Aspose.Words](../../../)
