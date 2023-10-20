---
title: Document.Clone
linktitle: Clone
articleTitle: Clone
second_title: Aspose.Words for .NET
description: Document Clone yöntem. Derin bir kopyasını gerçekleştirir.Document  C#'da.
type: docs
weight: 550
url: /tr/net/aspose.words/document/clone/
---
## Document.Clone method

Derin bir kopyasını gerçekleştirir.[`Document`](../) .

```csharp
public Document Clone()
```

### Geri dönüş değeri

Klonlanmış belge.

## Örnekler

Bir belgenin nasıl derinlemesine klonlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

// Klonlama orijinaliyle aynı içeriğe sahip yeni bir belge üretecek,
// ancak orijinal belgenin düğümlerinin her birinin benzersiz bir kopyasıyla.
Document clone = doc.Clone();

Assert.AreEqual(doc.FirstSection.Body.FirstParagraph.Runs[0].GetText(), 
    clone.FirstSection.Body.FirstParagraph.Runs[0].Text);
Assert.AreNotEqual(doc.FirstSection.Body.FirstParagraph.Runs[0].GetHashCode(),
    clone.FirstSection.Body.FirstParagraph.Runs[0].GetHashCode());
```

### Ayrıca bakınız

* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
