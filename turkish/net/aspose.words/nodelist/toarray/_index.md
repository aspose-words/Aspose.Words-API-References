---
title: NodeList.ToArray
linktitle: ToArray
articleTitle: ToArray
second_title: Aspose.Words for .NET
description: NodeList ToArray yöntem. Koleksiyondaki tüm düğümleri yeni bir düğüm dizisine kopyalar C#'da.
type: docs
weight: 40
url: /tr/net/aspose.words/nodelist/toarray/
---
## NodeList.ToArray method

Koleksiyondaki tüm düğümleri yeni bir düğüm dizisine kopyalar.

```csharp
public Node[] ToArray()
```

### Geri dönüş değeri

Bir dizi düğüm.

## Notlar

Yineleyiciyi geçersiz kıldığından ve canlı koleksiyonlar için yenilemeler gerektirdiğinden, düğüm koleksiyonu üzerinde yineleme yaparken düğüm eklememeli/kaldırmamalısınız.

Yineleme sırasında düğümleri ekleyebilmek/kaldırabilmek için, düğümlerini sabit boyutlu bir diziye kopyalamak ve ardından dizi üzerinde yineleme yapmak için bu yöntemi kullanın.

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
* class [NodeList](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
