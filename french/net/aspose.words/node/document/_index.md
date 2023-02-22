---
title: Node.Document
second_title: Référence de l'API Aspose.Words pour .NET
description: Node propriété. Obtient le document auquel ce nœud appartient.
type: docs
weight: 20
url: /fr/net/aspose.words/node/document/
---
## Node.Document property

Obtient le document auquel ce nœud appartient.

```csharp
public virtual DocumentBase Document { get; }
```

### Remarques

Le nœud appartient toujours à un document même s'il vient d'être créé et pas encore ajouté à l'arborescence, ou s'il a été supprimé de l'arborescence.

### Exemples

Montre comment créer un nœud et définir son document propriétaire.

```csharp
Document doc = new Document();
Paragraph para = new Paragraph(doc);
para.AppendChild(new Run(doc, "Hello world!"));

// Nous n'avons pas encore ajouté ce paragraphe en tant qu'enfant à un nœud composite.
Assert.IsNull(para.ParentNode);

// Si un nœud est un type de nœud enfant approprié d'un autre nœud composite,
// nous ne pouvons l'attacher en tant qu'enfant que si les deux nœuds ont le même document propriétaire.
// Le document propriétaire est le document que nous avons passé au constructeur du nœud.
// Nous n'avons pas attaché ce paragraphe au document, donc le document ne contient pas son texte.
Assert.AreEqual(para.Document, doc);
Assert.AreEqual(string.Empty, doc.GetText().Trim());

// Puisque le document possède ce paragraphe, nous pouvons appliquer un de ses styles au contenu du paragraphe.
para.ParagraphFormat.Style = doc.Styles["Heading 1"];

// Ajoutez ce nœud au document, puis vérifiez son contenu.
doc.FirstSection.Body.AppendChild(para);

Assert.AreEqual(doc.FirstSection.Body, para.ParentNode);
Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Voir également

* class [DocumentBase](../../documentbase/)
* class [Node](../)
* espace de noms [Aspose.Words](../../node/)
* Assemblée [Aspose.Words](../../../)


