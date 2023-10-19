---
title: CompositeNode.SelectSingleNode
linktitle: SelectSingleNode
articleTitle: SelectSingleNode
second_title: Aspose.Words for .NET
description: CompositeNode SelectSingleNode yöntem. İlkini seçerNode XPath ifadesiyle eşleşen C#'da.
type: docs
weight: 200
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

İlk[`Node`](../../node/) XPath sorgusuyla eşleşen veya`hükümsüz` eşleşen düğüm bulunamazsa.

## Notlar

Şu anda yalnızca öğe adlarına sahip ifadeler desteklenmektedir. Öznitelik adlarını kullanan Expressions desteklenmez.

## Örnekler

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

* class [Node](../../node/)
* class [CompositeNode](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
