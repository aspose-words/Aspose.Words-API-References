---
title: NodeList.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: .NET için Aspose.Words
description: GetEnumerator metoduyla NodeList'te zahmetsizce yineleme yapın. C#'ta düğüm koleksiyonunuza basit ve etkili erişimin tadını çıkarın.
type: docs
weight: 30
url: /tr/net/aspose.words/nodelist/getenumerator/
---
## NodeList.GetEnumerator method

Düğüm koleksiyonu üzerinde basit bir "foreach" tarzı yineleme sağlar.

```csharp
public IEnumerator<Node> GetEnumerator()
```

### Geri dönüş değeri

Bir IEnumerator.

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
* class [NodeList](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
