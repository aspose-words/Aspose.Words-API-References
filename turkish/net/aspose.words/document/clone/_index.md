---
title: Document.Clone
linktitle: Clone
articleTitle: Clone
second_title: .NET için Aspose.Words
description: Belgelerinizi Belge Klonlama yöntemimizle zahmetsizce çoğaltın. Sorunsuz düzenleme ve verimli iş akışı için hassas derin kopyalar elde edin.
type: docs
weight: 590
url: /tr/net/aspose.words/document/clone/
---
## Document.Clone method

Derin bir kopyasını gerçekleştirir[`Document`](../) .

```csharp
public Document Clone()
```

### Geri dönüş değeri

Klonlanmış belge.

## Örnekler

Bir belgenin nasıl derin klonlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

// Klonlama, orijinaliyle aynı içeriğe sahip yeni bir belge üretecektir.
// ancak orijinal belgenin her bir düğümünün benzersiz bir kopyasıyla.
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
