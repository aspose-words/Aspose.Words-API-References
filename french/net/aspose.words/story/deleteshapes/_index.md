---
title: Story.DeleteShapes
linktitle: DeleteShapes
articleTitle: DeleteShapes
second_title: Aspose.Words pour .NET
description: Supprimez facilement toutes les formes du texte de votre récit grâce à la méthode DeleteShapes. Simplifiez votre contenu et gagnez en clarté dès aujourd'hui !
type: docs
weight: 70
url: /fr/net/aspose.words/story/deleteshapes/
---
## Story.DeleteShapes method

Supprime toutes les formes du texte de cette histoire.

```csharp
public void DeleteShapes()
```

## Exemples

Montre comment supprimer toutes les formes d'un nœud.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Utilisez un DocumentBuilder pour insérer une forme. Il s'agit d'une forme en ligne.
// qui a un paragraphe parent, qui est un nœud enfant du corps de la première section.
builder.InsertShape(ShapeType.Cube, 100.0, 100.0);

Assert.AreEqual(1, doc.GetChildNodes(NodeType.Shape, true).Count);

// Nous pouvons supprimer toutes les formes des paragraphes enfants de ce corps.
Assert.AreEqual(StoryType.MainText, doc.FirstSection.Body.StoryType);
doc.FirstSection.Body.DeleteShapes();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Shape, true).Count);
```

### Voir également

* class [Story](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
