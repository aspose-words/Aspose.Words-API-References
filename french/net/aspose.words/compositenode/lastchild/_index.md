---
title: CompositeNode.LastChild
second_title: Référence de l'API Aspose.Words pour .NET
description: CompositeNode propriété. Obtient le dernier enfant du nœud.
type: docs
weight: 50
url: /fr/net/aspose.words/compositenode/lastchild/
---
## CompositeNode.LastChild property

Obtient le dernier enfant du nœud.

```csharp
public Node LastChild { get; }
```

### Remarques

S'il n'y a pas de dernier nœud enfant, un`nul` est renvoyé.

### Exemples

Montre comment utiliser les méthodes Node et CompositeNode pour supprimer une section avant la dernière section du document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Section 1 text.");
builder.InsertBreak(BreakType.SectionBreakContinuous);
builder.Writeln("Section 2 text.");

// Les deux sections sont frères et sœurs l'un de l'autre.
Section lastSection = (Section)doc.LastChild;
Section firstSection = (Section)lastSection.PreviousSibling;

// Supprime une section en fonction de sa relation fraternelle avec une autre section.
if (lastSection.PreviousSibling != null)
    doc.RemoveChild(firstSection);

// La section que nous avons supprimée était la première, ne laissant dans le document que la seconde.
Assert.AreEqual("Section 2 text.", doc.GetText().Trim());
```

### Voir également

* class [Node](../../node/)
* class [CompositeNode](../)
* espace de noms [Aspose.Words](../../compositenode/)
* Assemblée [Aspose.Words](../../../)


