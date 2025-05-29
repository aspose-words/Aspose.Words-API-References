---
title: NodeCollection.Add
linktitle: Add
articleTitle: Add
second_title: .NET için Aspose.Words
description: Koleksiyonunuza düğümleri zahmetsizce eklemek için NodeCollection Add yöntemini keşfedin, böylece veri yönetiminizi kolay ve verimli bir şekilde geliştirin.
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
| NotSupportedException | The[`NodeCollection`](../) "derin" bir koleksiyondur. |

## Notlar

Düğüm, koleksiyonun oluşturulduğu düğüm nesnesine bir çocuk olarak eklenir.

Eklenen düğüm başka bir belgeden oluşturulduysa, kullanmalısınız[`ImportNode`](../../documentbase/importnode/) Düğümü geçerli belgeye aktarmak için. Daha sonra içe aktarılan düğüm geçerli belgeye eklenebilir.

## Örnekler

Yeni bir bölüm düğümünün düzenlemeye nasıl hazırlanacağını gösterir.

```csharp
Document doc = new Document();

// Boş bir belge, bir gövdeye sahip bir bölüm ve gövdenin de bir paragrafı ile birlikte gelir.
// Bu paragrafa metin bölümleri, şekiller veya tablolar gibi öğeler ekleyerek belgeye içerik ekleyebiliriz.
Assert.AreEqual(NodeType.Section, doc.GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Body, doc.Sections[0].GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Paragraph, doc.Sections[0].Body.GetChild(NodeType.Any, 0, true).NodeType);

// Eğer bu şekilde yeni bir bölüm eklersek, bir gövdesi veya başka herhangi bir alt düğümü olmayacaktır.
doc.Sections.Add(new Section(doc));

Assert.AreEqual(0, doc.Sections[1].GetChildNodes(NodeType.Any, true).Count);

// Bu bölümü düzenlemeye başlamak için "EnsureMinimum" metodunu çalıştırarak bir gövde ve bir paragraf ekleyin.
doc.LastSection.EnsureMinimum();

Assert.AreEqual(NodeType.Body, doc.Sections[1].GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Paragraph, doc.Sections[1].Body.GetChild(NodeType.Any, 0, true).NodeType);

doc.Sections[0].Body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Ayrıca bakınız

* class [Node](../../node/)
* class [NodeCollection](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
