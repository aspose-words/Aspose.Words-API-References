---
title: ParagraphCollection.ToArray
second_title: Référence de l'API Aspose.Words pour .NET
description: ParagraphCollection méthode. Copie tous les paragraphes de la collection dans un nouveau tableau de paragraphes.
type: docs
weight: 20
url: /fr/net/aspose.words/paragraphcollection/toarray/
---
## ParagraphCollection.ToArray method

Copie tous les paragraphes de la collection dans un nouveau tableau de paragraphes.

```csharp
public Paragraph[] ToArray()
```

### Return_Value

Un tableau de paragraphes.

### Exemples

Montre comment créer un tableau à partir d'un NodeCollection.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

Paragraph[] paras = doc.FirstSection.Body.Paragraphs.ToArray();

Assert.AreEqual(22, paras.Length);
```

Montre comment utiliser « hot remove » pour supprimer un nœud lors de l'énumération.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("The first paragraph");
builder.Writeln("The second paragraph");
builder.Writeln("The third paragraph");
builder.Writeln("The fourth paragraph");

// Supprime un nœud de la collection au milieu d'une énumération.
foreach (Paragraph para in doc.FirstSection.Body.Paragraphs.ToArray())
    if (para.Range.Text.Contains("third"))
        para.Remove();

Assert.False(doc.GetText().Contains("The third paragraph"));
```

### Voir également

* class [Paragraph](../../paragraph/)
* class [ParagraphCollection](../)
* espace de noms [Aspose.Words](../../paragraphcollection/)
* Assemblée [Aspose.Words](../../../)


