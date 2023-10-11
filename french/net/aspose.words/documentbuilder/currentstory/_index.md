---
title: DocumentBuilder.CurrentStory
second_title: Référence de l'API Aspose.Words pour .NET
description: DocumentBuilder propriété. Obtient lhistoire actuellement sélectionnée dans ceDocumentBuilder .
type: docs
weight: 70
url: /fr/net/aspose.words/documentbuilder/currentstory/
---
## DocumentBuilder.CurrentStory property

Obtient l'histoire actuellement sélectionnée dans ce[`DocumentBuilder`](../) .

```csharp
public Story CurrentStory { get; }
```

### Exemples

Montre comment travailler avec l'histoire actuelle d'un générateur de documents.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Une histoire est un type de nœud qui a des nœuds paragraphe enfants, tels qu'un corps.
Assert.AreEqual(builder.CurrentStory, doc.FirstSection.Body);
Assert.AreEqual(builder.CurrentStory, builder.CurrentParagraph.ParentNode);
Assert.AreEqual(StoryType.MainText, builder.CurrentStory.StoryType);

builder.CurrentStory.AppendParagraph("Text added to current Story.");

// Une Story peut également contenir des tableaux.
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
* espace de noms [Aspose.Words](../../documentbuilder/)
* Assemblée [Aspose.Words](../../../)


