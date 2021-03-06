---
title: RemoveChild
second_title: Référence de l'API Aspose.Words pour .NET
description: Supprime le nœud enfant spécifié.
type: docs
weight: 180
url: /fr/net/aspose.words/compositenode/removechild/
---
## CompositeNode.RemoveChild method

Supprime le nœud enfant spécifié.

```csharp
public Node RemoveChild(Node oldChild)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| oldChild | Node | Le nœud à supprimer. |

### Return_Value

Le nœud supprimé.

### Remarques

Le parent de oldChild est défini sur null après la suppression du nœud.

### Exemples

Montre comment utiliser les méthodes de Node et CompositeNode pour supprimer une section avant la dernière section du document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Section 1 text.");
builder.InsertBreak(BreakType.SectionBreakContinuous);
builder.Writeln("Section 2 text.");

// Les deux sections sont frères l'une de l'autre.
Section lastSection = (Section)doc.LastChild;
Section firstSection = (Section)lastSection.PreviousSibling;

// Supprime une section en fonction de sa relation de fratrie avec une autre section.
if (lastSection.PreviousSibling != null)
    doc.RemoveChild(firstSection);

// La section que nous avons supprimée était la première, laissant le document avec seulement la seconde.
Assert.AreEqual("Section 2 text.", doc.GetText().Trim());
```

### Voir également

* class [Node](../../node)
* class [CompositeNode](../../compositenode)
* espace de noms [Aspose.Words](../../compositenode)
* Assemblée [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
