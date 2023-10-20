---
title: Comment.SetText
linktitle: SetText
articleTitle: SetText
second_title: Aspose.Words pour .NET
description: Comment SetText méthode. Il sagit dune méthode pratique qui permet de définir facilement le texte du commentaire en C#.
type: docs
weight: 150
url: /fr/net/aspose.words/comment/settext/
---
## Comment.SetText method

Il s'agit d'une méthode pratique qui permet de définir facilement le texte du commentaire.

```csharp
public void SetText(string text)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| text | String | Le nouveau texte du commentaire. |

## Remarques

Cette méthode permet de définir rapidement le texte d'un commentaire à partir d'une chaîne. La chaîne peut contenir des sauts de paragraphe , cela créera des paragraphes de texte dans le commentaire en conséquence. Si vous souhaitez insérer des éléments plus complexes dans le commentaire, par exemple bookmarks ou des tableaux ou appliquer une mise en forme riche, vous devez alors utiliser les classes de nœuds appropriées. pour construire le texte du commentaire.

## Exemples

Montre comment ajouter un commentaire à un document, puis y répondre.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");

// Place le commentaire à un nœud du corps du document.
// Ce commentaire apparaîtra à l'emplacement de son paragraphe,
// en dehors de la marge droite de la page, et avec une ligne pointillée la reliant à son paragraphe.
builder.CurrentParagraph.AppendChild(comment);

// Ajoute une réponse, qui apparaîtra sous son commentaire parent.
comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "New reply");

// Les commentaires et les réponses sont tous deux des nœuds de commentaires.
Assert.AreEqual(2, doc.GetChildNodes(NodeType.Comment, true).Count);

// Les commentaires qui ne répondent pas aux autres commentaires sont du "niveau supérieur". Ils n'ont aucun commentaire d'ancêtre.
Assert.Null(comment.Ancestor);

// Les réponses ont un commentaire de niveau supérieur ancêtre.
Assert.AreEqual(comment, comment.Replies[0].Ancestor);

doc.Save(ArtifactsDir + "Comment.AddCommentWithReply.docx");
```

### Voir également

* class [Comment](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
