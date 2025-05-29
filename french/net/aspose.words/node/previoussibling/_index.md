---
title: Node.PreviousSibling
linktitle: PreviousSibling
articleTitle: PreviousSibling
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Node PreviousSibling pour accéder facilement au nœud qui précède votre nœud actuel, améliorant ainsi vos compétences en manipulation DOM.
type: docs
weight: 70
url: /fr/net/aspose.words/node/previoussibling/
---
## Node.PreviousSibling property

Obtient le nœud précédant immédiatement ce nœud.

```csharp
public Node PreviousSibling { get; }
```

## Remarques

S'il n'y a pas de nœud précédent, un`nul` est renvoyé.

## Exemples

Montre comment utiliser les méthodes Node et CompositeNode pour supprimer une section avant la dernière section du document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Section 1 text.");
builder.InsertBreak(BreakType.SectionBreakContinuous);
builder.Writeln("Section 2 text.");

// Les deux sections sont sœurs l'une de l'autre.
Section lastSection = (Section)doc.LastChild;
Section firstSection = (Section)lastSection.PreviousSibling;

// Supprimez une section en fonction de sa relation de fratrie avec une autre section.
if (lastSection.PreviousSibling != null)
    doc.RemoveChild(firstSection);

// La section que nous avons supprimée était la première, ne laissant dans le document que la seconde.
Assert.AreEqual("Section 2 text.", doc.GetText().Trim());
```

### Voir également

* class [Node](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
