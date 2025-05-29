---
title: CompositeNode.RemoveChild
linktitle: RemoveChild
articleTitle: RemoveChild
second_title: Aspose.Words pour .NET
description: Gérez sans effort votre CompositeNode avec la méthode RemoveChild, conçue pour rationaliser la suppression des nœuds pour des performances et une efficacité améliorées.
type: docs
weight: 190
url: /fr/net/aspose.words/compositenode/removechild/
---
## CompositeNode.RemoveChild&lt;T&gt; method

Supprime le nœud enfant spécifié.

```csharp
public T RemoveChild<T>(T oldChild)
    where T : Node
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| oldChild | T | Le nœud à supprimer. |

### Return_Value

Le nœud supprimé.

## Remarques

Le parent de*oldChild* est réglé sur`nul` après le retrait du nœud.

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

* class [Node](../../node/)
* class [CompositeNode](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
