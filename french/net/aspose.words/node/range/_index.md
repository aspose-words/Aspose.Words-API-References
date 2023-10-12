---
title: Node.Range
second_title: Référence de l'API Aspose.Words pour .NET
description: Node propriété. Renvoie unRange objet qui représente la partie dun document contenue dans ce nœud.
type: docs
weight: 80
url: /fr/net/aspose.words/node/range/
---
## Node.Range property

Renvoie un[`Range`](../../range/) objet qui représente la partie d'un document contenue dans ce nœud.

```csharp
public Range Range { get; }
```

### Exemples

Montre comment supprimer tous les nœuds d’une plage.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ajoutez du texte à la première section du document, puis ajoutez une autre section.
builder.Write("Section 1. ");
builder.InsertBreak(BreakType.SectionBreakContinuous);
builder.Write("Section 2.");

Assert.AreEqual("Section 1. \fSection 2.", doc.GetText().Trim());

// Supprime entièrement la première section en supprimant tous les nœuds
// dans sa plage, y compris la section elle-même.
doc.Sections[0].Range.Delete();

Assert.AreEqual(1, doc.Sections.Count);
Assert.AreEqual("Section 2.", doc.GetText().Trim());
```

### Voir également

* class [Range](../../range/)
* class [Node](../)
* espace de noms [Aspose.Words](../../node/)
* Assemblée [Aspose.Words](../../../)


