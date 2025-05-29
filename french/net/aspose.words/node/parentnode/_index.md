---
title: Node.ParentNode
linktitle: ParentNode
articleTitle: ParentNode
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Node ParentNode pour accéder facilement au parent immédiat de n'importe quel nœud, améliorant ainsi l'efficacité de votre développement Web et la clarté de votre code.
type: docs
weight: 60
url: /fr/net/aspose.words/node/parentnode/
---
## Node.ParentNode property

Obtient le parent immédiat de ce nœud.

```csharp
public CompositeNode ParentNode { get; }
```

## Remarques

Si un nœud vient d'être créé et n'est pas encore ajouté à l'arbre, ou s'il a été supprimé de l'arbre, le parent est`nul`.

## Exemples

Montre comment accéder au nœud parent d'un nœud.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// Ajouter un nœud Run enfant au premier paragraphe du document.
Run run = new Run(doc, "Hello world!");
para.AppendChild(run);

// Le paragraphe est le nœud parent du nœud d'exécution. Nous pouvons retracer cette lignée.
// jusqu'au nœud du document, qui est la racine de l'arborescence des nœuds du document.
Assert.AreEqual(para, run.ParentNode);
Assert.AreEqual(doc.FirstSection.Body, para.ParentNode);
Assert.AreEqual(doc.FirstSection, doc.FirstSection.Body.ParentNode);
Assert.AreEqual(doc, doc.FirstSection.ParentNode);
```

Montre comment créer un nœud et définir son document propriétaire.

```csharp
Document doc = new Document();
Paragraph para = new Paragraph(doc);
para.AppendChild(new Run(doc, "Hello world!"));

// Nous n'avons pas encore ajouté ce paragraphe en tant qu'enfant à un nœud composite.
Assert.IsNull(para.ParentNode);

// Si un nœud est un type de nœud enfant approprié d'un autre nœud composite,
// nous pouvons l'attacher en tant qu'enfant uniquement si les deux nœuds ont le même document propriétaire.
// Le document propriétaire est le document que nous avons transmis au constructeur du nœud.
// Nous n'avons pas joint ce paragraphe au document, donc le document ne contient pas son texte.
Assert.AreEqual(para.Document, doc);
Assert.AreEqual(string.Empty, doc.GetText().Trim());

// Étant donné que le document possède ce paragraphe, nous pouvons appliquer l'un de ses styles au contenu du paragraphe.
para.ParagraphFormat.Style = doc.Styles["Heading 1"];

// Ajoutez ce nœud au document, puis vérifiez son contenu.
doc.FirstSection.Body.AppendChild(para);

Assert.AreEqual(doc.FirstSection.Body, para.ParentNode);
Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Voir également

* class [CompositeNode](../../compositenode/)
* class [Node](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
