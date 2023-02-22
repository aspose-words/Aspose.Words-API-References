---
title: Class CommentCollection
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.CommentCollection classe. Fournit un accès typé à une collection deComment nœuds.
type: docs
weight: 230
url: /fr/net/aspose.words/commentcollection/
---
## CommentCollection class

Fournit un accès typé à une collection de[`Comment`](../comment/) nœuds.

```csharp
public class CommentCollection : NodeCollection
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | Obtient le nombre de nœuds dans la collection. |
| [Item](../../aspose.words/commentcollection/item/) { get; } | Récupère un **Commentaire** à l'index donné. (2 indexers) |

## Méthodes

| Nom | La description |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(Node) | Ajoute un nœud à la fin de la collection. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Supprime tous les nœuds de cette collection et du document. |
| [Contains](../../aspose.words/nodecollection/contains/)(Node) | Détermine si un nœud est dans la collection. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | Fournit une simple itération de style "foreach" sur la collection de nœuds. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(Node) | Renvoie l'index de base zéro du nœud spécifié. |
| [Insert](../../aspose.words/nodecollection/insert/)(int, Node) | Insère un nœud dans la collection à l'index spécifié. |
| [Remove](../../aspose.words/nodecollection/remove/)(Node) | Supprime le nœud de la collection et du document. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(int) | Supprime le nœud à l'index spécifié de la collection et du document. |
| [ToArray](../../aspose.words/nodecollection/toarray/)() | Copie tous les nœuds de la collection vers un nouveau tableau de nœuds. |

### Exemples

Montre comment marquer un commentaire comme "terminé".

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Helo world!");

// Insère un commentaire pour signaler une erreur. 
Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("Fix the spelling error!");
doc.FirstSection.Body.FirstParagraph.AppendChild(comment);

// Les commentaires ont un indicateur "Done", qui est défini sur "false" par défaut. 
// Si un commentaire suggère que nous fassions un changement dans le document,
// nous pouvons appliquer la modification, puis définir ensuite le drapeau "Done" pour indiquer la correction.
Assert.False(comment.Done);

doc.FirstSection.Body.FirstParagraph.Runs[0].Text = "Hello world!";
comment.Done = true;

// Les commentaires "faits" se différencieront
// de ceux qui ne sont pas "terminés" avec une couleur de texte fanée.
comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("Add text to this paragraph.");
builder.CurrentParagraph.AppendChild(comment);

doc.Save(ArtifactsDir + "Comment.Done.docx");
```

### Voir également

* class [NodeCollection](../nodecollection/)
* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)


