---
title: CommentCollection Class
linktitle: CommentCollection
articleTitle: CommentCollection
second_title: Aspose.Words pour .NET
description: Aspose.Words.CommentCollection classe. Fournit un accès typé à une collection deComment nœuds en C#.
type: docs
weight: 240
url: /fr/net/aspose.words/commentcollection/
---
## CommentCollection class

Fournit un accès typé à une collection de[`Comment`](../comment/) nœuds.

Pour en savoir plus, visitez le[Travailler avec des commentaires](https://docs.aspose.com/words/net/working-with-comments/) article documentaire.

```csharp
public class CommentCollection : NodeCollection
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | Obtient le nombre de nœuds dans la collection. |
| [Item](../../aspose.words/commentcollection/item/) { get; } | Récupère un[`Comment`](../comment/) à l'index donné. (2 indexers) |

## Méthodes

| Nom | La description |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(*[Node](../node/)*) | Ajoute un nœud à la fin de la collection. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Supprime tous les nœuds de cette collection et du document. |
| [Contains](../../aspose.words/nodecollection/contains/)(*[Node](../node/)*) | Détermine si un nœud fait partie de la collection. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | Fournit une simple itération de style "foreach" sur la collection de nœuds. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(*[Node](../node/)*) | Renvoie l'index de base zéro du nœud spécifié. |
| [Insert](../../aspose.words/nodecollection/insert/)(*int, [Node](../node/)*) | Insère un nœud dans la collection à l'index spécifié. |
| [Remove](../../aspose.words/nodecollection/remove/)(*[Node](../node/)*) | Supprime le nœud de la collection et du document. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(*int*) | Supprime le nœud à l'index spécifié de la collection et du document. |
| [ToArray](../../aspose.words/nodecollection/toarray/)() | Copie tous les nœuds de la collection vers un nouveau tableau de nœuds. |

## Exemples

Montre comment marquer un commentaire comme « terminé ».

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Helo world!");

 // Insère un commentaire pour signaler une erreur.
Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("Fix the spelling error!");
doc.FirstSection.Body.FirstParagraph.AppendChild(comment);

 // Les commentaires ont un indicateur "Terminé", qui est défini sur "false" par défaut.
// Si un commentaire nous suggère d'effectuer une modification au sein du document,
// nous pouvons appliquer la modification, puis également définir le drapeau "Terminé" par la suite pour indiquer la correction.
Assert.False(comment.Done);

doc.FirstSection.Body.FirstParagraph.Runs[0].Text = "Hello world!";
comment.Done = true;

// Les commentaires "terminés" se différencieront
// parmi ceux qui ne sont pas "finis" avec une couleur de texte délavée.
comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("Add text to this paragraph.");
builder.CurrentParagraph.AppendChild(comment);

doc.Save(ArtifactsDir + "Comment.Done.docx");
```

### Voir également

* class [NodeCollection](../nodecollection/)
* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
