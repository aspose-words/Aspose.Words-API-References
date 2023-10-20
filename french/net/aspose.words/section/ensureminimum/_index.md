---
title: Section.EnsureMinimum
linktitle: EnsureMinimum
articleTitle: EnsureMinimum
second_title: Aspose.Words pour .NET
description: Section EnsureMinimum méthode. Garantit que la section aBody avec unParagraph  en C#.
type: docs
weight: 130
url: /fr/net/aspose.words/section/ensureminimum/
---
## Section.EnsureMinimum method

Garantit que la section a[`Body`](../body/) avec un[`Paragraph`](../../paragraph/) .

```csharp
public void EnsureMinimum()
```

## Exemples

Montre comment préparer un nouveau nœud de section pour la modification.

```csharp
Document doc = new Document();

// Un document vierge est livré avec une section, qui a un corps, qui à son tour contient un paragraphe.
// Nous pouvons ajouter du contenu à ce document en ajoutant des éléments tels que des passages de texte, des formes ou des tableaux à ce paragraphe.
Assert.AreEqual(NodeType.Section, doc.GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Body, doc.Sections[0].GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Paragraph, doc.Sections[0].Body.GetChild(NodeType.Any, 0, true).NodeType);

// Si nous ajoutons une nouvelle section comme celle-ci, elle n'aura pas de corps, ni aucun autre nœud enfant.
doc.Sections.Add(new Section(doc));

Assert.AreEqual(0, doc.Sections[1].GetChildNodes(NodeType.Any, true).Count);

// Exécutez la méthode "EnsureMinimum" pour ajouter un corps et un paragraphe à cette section et commencer à la modifier.
doc.LastSection.EnsureMinimum();

Assert.AreEqual(NodeType.Body, doc.Sections[1].GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Paragraph, doc.Sections[1].Body.GetChild(NodeType.Any, 0, true).NodeType);

doc.Sections[0].Body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Voir également

* class [Section](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
