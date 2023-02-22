---
title: CompositeNode.SelectSingleNode
second_title: Aspose.Words for .NET API Referansı
description: CompositeNode yöntem. XPath ifadesiyle eşleşen ilk Düğümü seçer.
type: docs
weight: 210
url: /tr/net/aspose.words/compositenode/selectsinglenode/
---
## CompositeNode.SelectSingleNode method

XPath ifadesiyle eşleşen ilk Düğümü seçer.

```csharp
public Node SelectSingleNode(string xpath)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| xpath | String | XPath ifadesi. |

### Geri dönüş değeri

XPath sorgusuyla eşleşen ilk Düğüm veya eşleşen bir düğüm bulunamazsa null.

### Notlar

Şu anda yalnızca öğe adlarına sahip ifadeler desteklenmektedir. Öznitelik adlarını kullanan Expressions desteklenmez.

### Örnekler

Bir XPath ifadesi kullanarak belirli düğümlerin nasıl seçileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

// Bu ifade tüm paragraf düğümlerini çıkaracak,
// belgedeki herhangi bir tablo düğümünün soyundan gelenler.
NodeList nodeList = doc.SelectNodes("//Tablo//Paragraf");

// Listeyi bir numaralandırıcı ile yineleyin ve tablonun her hücresindeki her paragrafın içeriğini yazdırın.
int index = 0;

using (IEnumerator<Node> e = nodeList.GetEnumerator())
    while (e.MoveNext())
        Console.WriteLine($"Table paragraph index {index++}, contents: \"{e.Current.GetText().Trim()}\"");

// Bu ifade, belgedeki herhangi bir Gövde düğümünün doğrudan çocukları olan tüm paragrafları seçecektir.
nodeList = doc.SelectNodes("//Gelişme paragrafı");

// Listeyi bir dizi olarak ele alabiliriz.
Assert.AreEqual(4, nodeList.ToArray().Length);

// Yukarıdakiyle aynı ifadenin ilk sonucunu seçmek için SelectSingleNode'u kullanın.
Node node = doc.SelectSingleNode("//Gelişme paragrafı");

Assert.AreEqual(typeof(Paragraph), node.GetType());
```

### Ayrıca bakınız

* class [Node](../../node/)
* class [CompositeNode](../)
* ad alanı [Aspose.Words](../../compositenode/)
* toplantı [Aspose.Words](../../../)


