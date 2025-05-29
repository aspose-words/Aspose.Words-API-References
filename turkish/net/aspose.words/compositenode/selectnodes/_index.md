---
title: CompositeNode.SelectNodes
linktitle: SelectNodes
articleTitle: SelectNodes
second_title: .NET için Aspose.Words
description: Gelişmiş veri işleme ve sorunsuz kodlama için XPath ifadelerini kullanarak CompositeNode SelectNodes yöntemiyle düğümleri zahmetsizce alın.
type: docs
weight: 210
url: /tr/net/aspose.words/compositenode/selectnodes/
---
## CompositeNode.SelectNodes method

XPath ifadesiyle eşleşen düğümlerin bir listesini seçer.

```csharp
public NodeList SelectNodes(string xpath)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| xpath | String | XPath ifadesi. |

### Geri dönüş değeri

XPath sorgusuyla eşleşen düğümlerin listesi.

## Notlar

Şu anda yalnızca öğe adlarına sahip ifadeler destekleniyor. Öznitelik adlarını kullanan Expressions desteklenmiyor.

## Örnekler

Bir düğümün bir alanın içinde olup olmadığını test etmek için bir XPath ifadesinin nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Mail merge destination - Northwind employees.docx");

// Bu XPath ifadesinden elde edilen NodeList, bir alan içerisinde bulduğumuz tüm düğümleri içerecektir.
// Ancak, yolda iç içe geçmiş alanlar varsa, FieldStart ve FieldEnd düğümleri listede olabilir.
// Şu anda FieldCode veya FieldResult'un birden fazla paragrafı kapsadığı nadir alanlar bulunmuyor.
NodeList resultList =
    doc.SelectNodes("//FieldStart/takip eden-kardeş::node()[takip eden-kardeş::FieldEnd]");

// Belirtilen çalışmanın alanın içindeki düğümlerden biri olup olmadığını kontrol et.
Console.WriteLine($"Contents of the first Run node that's part of a field: {resultList.First(n => n.NodeType == NodeType.Run).GetText().Trim()}");
```

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

* class [NodeList](../../nodelist/)
* class [CompositeNode](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
