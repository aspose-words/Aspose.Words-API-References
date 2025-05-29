---
title: CommentCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words pour .NET
description: Accédez facilement à des commentaires spécifiques grâce à la propriété Élément CommentCollection. Récupérez les commentaires par index pour une gestion de contenu simplifiée.
type: docs
weight: 10
url: /fr/net/aspose.words/commentcollection/item/
---
## CommentCollection indexer

Récupère un[`Comment`](../../comment/) à l'index donné.

```csharp
public Comment this[int index] { get; }
```

| Paramètre | La description |
| --- | --- |
| index | Un index de la collection. |

## Remarques

L'indice est basé sur zéro.

Les index négatifs sont autorisés et indiquent l'accès depuis l'arrière de la collection. Par exemple, -1 signifie le dernier élément, -2 signifie l'avant-dernier et ainsi de suite.

Si l'index est supérieur ou égal au nombre d'éléments dans la liste, cela renvoie une référence nulle.

Si l'index est négatif et que sa valeur absolue est supérieure au nombre d'éléments dans la liste, cela renvoie une référence nulle.

## Exemples

Montre comment supprimer les réponses aux commentaires.

```csharp
Document doc = new Document();

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");

doc.FirstSection.Body.FirstParagraph.AppendChild(comment);

comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "New reply");
comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "Another reply");

Assert.AreEqual(2, comment.Replies.Count); 

// Vous trouverez ci-dessous deux manières de supprimer les réponses d'un commentaire.
// 1 - Utilisez la méthode « RemoveReply » pour supprimer individuellement les réponses d'un commentaire :
comment.RemoveReply(comment.Replies[0]);

Assert.AreEqual(1, comment.Replies.Count);

// 2 - Utilisez la méthode « RemoveAllReplies » pour supprimer toutes les réponses d'un commentaire à la fois :
comment.RemoveAllReplies();

Assert.AreEqual(0, comment.Replies.Count);
```

### Voir également

* class [Comment](../../comment/)
* class [CommentCollection](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
