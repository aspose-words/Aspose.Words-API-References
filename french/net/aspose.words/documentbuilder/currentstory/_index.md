---
title: DocumentBuilder.CurrentStory
linktitle: CurrentStory
articleTitle: CurrentStory
second_title: Aspose.Words pour .NET
description: Découvrez la propriété CurrentStory de DocumentBuilder pour accéder et gérer efficacement l'histoire sélectionnée, améliorant ainsi votre expérience d'édition de documents.
type: docs
weight: 70
url: /fr/net/aspose.words/documentbuilder/currentstory/
---
## DocumentBuilder.CurrentStory property

Obtient l'histoire actuellement sélectionnée dans ce[`DocumentBuilder`](../) .

```csharp
public Story CurrentStory { get; }
```

## Exemples

Montre comment travailler avec l'histoire actuelle d'un générateur de documents.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Une histoire est un type de nœud qui a des nœuds de paragraphe enfants, comme un corps.
Assert.AreEqual(builder.CurrentStory, doc.FirstSection.Body);
Assert.AreEqual(builder.CurrentStory, builder.CurrentParagraph.ParentNode);
Assert.AreEqual(StoryType.MainText, builder.CurrentStory.StoryType);

builder.CurrentStory.AppendParagraph("Text added to current Story.");

// Une histoire peut également contenir des tableaux.
Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1");
builder.InsertCell();
builder.Write("Row 1, cell 2");
builder.EndTable();

Assert.IsTrue(builder.CurrentStory.Tables.Contains(table));
```

### Voir également

* class [Story](../../story/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
