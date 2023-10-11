---
title: NodeCollection.Add
second_title: Aspose.Words for .NET API Referansı
description: NodeCollection yöntem. Koleksiyonun sonuna bir düğüm ekler.
type: docs
weight: 30
url: /tr/net/aspose.words/nodecollection/add/
---
## NodeCollection.Add method

Koleksiyonun sonuna bir düğüm ekler.

```csharp
public void Add(Node node)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| node | Node | Koleksiyonun sonuna eklenecek düğüm. |

### istisnalar

| istisna | şart |
| --- | --- |
| NotSupportedException | [`NodeCollection`](../) "derin" bir koleksiyondur. |

### Notlar

Düğüm, koleksiyonun oluşturulduğu düğüm nesnesine alt öğe olarak eklenir.

Eklenen düğüm başka bir belgeden oluşturulmuşsa kullanmalısınız[`ImportNode`](../../documentbase/importnode/) Düğümü geçerli belgeye aktarmak için. İçe aktarılan düğüm daha sonra geçerli belgeye eklenebilir.

### Örnekler

Düzenleme için yeni bir bölüm düğümünün nasıl hazırlanacağını gösterir.

```csharp
Document doc = new Document();

// Boş bir belge, bir gövdeye sahip olan ve bunun da bir paragrafa sahip olduğu bir bölümle birlikte gelir.
// Bu paragrafa metin dizileri, şekiller veya tablolar gibi öğeler ekleyerek bu belgeye içerik ekleyebiliriz.
Assert.AreEqual(NodeType.Section, doc.GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Body, doc.Sections[0].GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Paragraph, doc.Sections[0].Body.GetChild(NodeType.Any, 0, true).NodeType);

// Bunun gibi yeni bir bölüm eklersek ne gövdesi ne de başka bir alt düğümü olmayacak.
doc.Sections.Add(new Section(doc));

Assert.AreEqual(0, doc.Sections[1].GetChildNodes(NodeType.Any, true).Count);

// Düzenlemeye başlamak için bu bölüme bir gövde ve paragraf eklemek üzere "EnsureMinimum" yöntemini çalıştırın.
doc.LastSection.EnsureMinimum();

Assert.AreEqual(NodeType.Body, doc.Sections[1].GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Paragraph, doc.Sections[1].Body.GetChild(NodeType.Any, 0, true).NodeType);

doc.Sections[0].Body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Ayrıca bakınız

* class [Node](../../node/)
* class [NodeCollection](../)
* ad alanı [Aspose.Words](../../nodecollection/)
* toplantı [Aspose.Words](../../../)


