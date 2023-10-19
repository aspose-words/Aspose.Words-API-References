---
title: CompositeNode.SelectNodes
linktitle: SelectNodes
articleTitle: SelectNodes
second_title: Aspose.Words for .NET
description: CompositeNode SelectNodes yöntem. XPath ifadesiyle eşleşen düğümlerin listesini seçer C#'da.
type: docs
weight: 190
url: /tr/net/aspose.words/compositenode/selectnodes/
---
## CompositeNode.SelectNodes method

XPath ifadesiyle eşleşen düğümlerin listesini seçer.

```csharp
public NodeList SelectNodes(string xpath)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| xpath | String | XPath ifadesi. |

### Geri dönüş değeri

XPath sorgusuyla eşleşen düğümlerin listesi.

## Notlar

Şu anda yalnızca öğe adlarına sahip ifadeler desteklenmektedir. Öznitelik adlarını kullanan Expressions desteklenmez.

## Örnekler

Bir düğümün bir alanın içinde olup olmadığını test etmek için XPath ifadesinin nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Mail merge destination - Northwind employees.docx");

// Bu XPath ifadesinden elde edilen NodeList, bir alanın içinde bulduğumuz tüm düğümleri içerecektir.
// Ancak yolda iç içe alanlar varsa FieldStart ve FieldEnd düğümleri listede olabilir.
// Şu anda FieldCode veya FieldResult'un birden fazla paragrafa yayıldığı nadir alanlar bulunmuyor.
NodeList resultList =
    doc.SelectNodes("//FieldStart/takip eden-kardeş::node()[takip eden-kardeş::FieldEnd]");

// Belirtilen çalıştırmanın alanın içindeki düğümlerden biri olup olmadığını kontrol edin.
Console.WriteLine($"Contents of the first Run node that's part of a field: {resultList.First(n => n.NodeType == NodeType.Run).GetText().Trim()}");
```

XPath ifadesini kullanarak belirli düğümlerin nasıl seçileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

// Bu ifade tüm paragraf düğümlerini çıkaracak,
// bunlar belgedeki herhangi bir tablo düğümünün alt öğeleridir.
NodeList nodeList = doc.SelectNodes("//Tablo//Paragraf");

// Listeyi bir numaralandırıcıyla yineleyin ve her paragrafın içeriğini tablonun her hücresine yazdırın.
int index = 0;

using (IEnumerator<Node> e = nodeList.GetEnumerator())
    while (e.MoveNext())
        Console.WriteLine($"Table paragraph index {index++}, contents: \"{e.Current.GetText().Trim()}\"");

// Bu ifade, belgedeki herhangi bir Gövde düğümünün doğrudan alt öğesi olan paragrafları seçecektir.
nodeList = doc.SelectNodes("//Gelişme paragrafı");

// Listeyi bir dizi gibi ele alabiliriz.
Assert.AreEqual(4, nodeList.ToArray().Length);

// Yukarıdakiyle aynı ifadenin ilk sonucunu seçmek için SelectSingleNode'u kullanın.
Node node = doc.SelectSingleNode("//Gelişme paragrafı");

Assert.AreEqual(typeof(Paragraph), node.GetType());
```

### Ayrıca bakınız

* class [NodeList](../../nodelist/)
* class [CompositeNode](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
