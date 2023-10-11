---
title: Story.StoryType
second_title: Référence de l'API Aspose.Words pour .NET
description: Story propriété. Obtient le type de cette histoire.
type: docs
weight: 40
url: /fr/net/aspose.words/story/storytype/
---
## Story.StoryType property

Obtient le type de cette histoire.

```csharp
public StoryType StoryType { get; }
```

### Exemples

Montre comment supprimer toutes les formes d’un nœud.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Utilisez un DocumentBuilder pour insérer une forme. Il s'agit d'une forme en ligne,
// qui a un paragraphe parent, qui est un nœud enfant du corps de la première section.
builder.InsertShape(ShapeType.Cube, 100.0, 100.0);

Assert.AreEqual(1, doc.GetChildNodes(NodeType.Shape, true).Count);

// Nous pouvons supprimer toutes les formes des paragraphes enfants de ce Body.
Assert.AreEqual(StoryType.MainText, doc.FirstSection.Body.StoryType);
doc.FirstSection.Body.DeleteShapes();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Shape, true).Count);
```

### Voir également

* enum [StoryType](../../storytype/)
* class [Story](../)
* espace de noms [Aspose.Words](../../story/)
* Assemblée [Aspose.Words](../../../)


