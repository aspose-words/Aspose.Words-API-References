---
title: CompositeNode.SelectSingleNode
linktitle: SelectSingleNode
articleTitle: SelectSingleNode
second_title: .NET için Aspose.Words
description: CompositeNode'un SelectSingleNode yönteminin, XPath ifadenizle eşleşen ilk Düğümü nasıl verimli bir şekilde alarak veri işlemeyi kolaylaştırdığını keşfedin.
type: docs
weight: 220
url: /tr/net/aspose.words/compositenode/selectsinglenode/
---
## CompositeNode.SelectSingleNode method

İlkini seçer[`Node`](../../node/) XPath ifadesiyle eşleşen.

```csharp
public Node SelectSingleNode(string xpath)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| xpath | String | XPath ifadesi. |

### Geri dönüş değeri

İlk[`Node`](../../node/) XPath sorgusuyla eşleşen veya`hükümsüz` eşleşen bir düğüm bulunamazsa.

## Notlar

Şu anda yalnızca öğe adlarına sahip ifadeler destekleniyor. Öznitelik adlarını kullanan Expressions desteklenmiyor.

## Örnekler

XPath ifadesi kullanılarak belirli düğümlerin nasıl seçileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

// Bu ifade tüm paragraf düğümlerini çıkaracaktır,
// belgedeki herhangi bir tablo düğümünün alt öğeleridir.
NodeList nodeList = doc.SelectNodes("//Tablo//Paragraf");

// Bir numaralandırıcı ile listede dolaş ve tablonun her hücresindeki her paragrafın içeriğini yazdır.
int index = 0;

using (IEnumerator<Node> e = nodeList.GetEnumerator())
    while (e.MoveNext())
        Console.WriteLine($"Table paragraph index {index++}, contents: \"{e.Current.GetText().Trim()}\"");

// Bu ifade, belgedeki herhangi bir Body düğümünün doğrudan alt öğesi olan tüm paragrafları seçecektir.
nodeList = doc.SelectNodes("//Gövde/Paragraf");

// Listeyi bir dizi olarak ele alabiliriz.
Assert.AreEqual(4, nodeList.ToArray().Length);

// Yukarıdaki ifadenin ilk sonucunu seçmek için SelectSingleNode'u kullanın.
Node node = doc.SelectSingleNode("//Gövde/Paragraf");

Assert.AreEqual(typeof(Paragraph), node.GetType());
```

### Ayrıca bakınız

* class [Node](../../node/)
* class [CompositeNode](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
