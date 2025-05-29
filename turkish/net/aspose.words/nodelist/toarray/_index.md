---
title: NodeList.ToArray
linktitle: ToArray
articleTitle: ToArray
second_title: .NET için Aspose.Words
description: ToArray metoduyla NodeList'i zahmetsizce diziye dönüştürerek düğüm manipülasyonunu basitleştirin ve web geliştirme iş akışınızı geliştirin.
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

düğümden oluşan bir koleksiyon üzerinde yineleme yaparken düğüm eklememeli/kaldırmamalısınız çünkü bu yineleyiciyi geçersiz kılar ve canlı koleksiyonlar için yenilemeler gerektirir.

Yineleme sırasında düğümleri ekleyip kaldırabilmek için, bu yöntemi kullanarak düğümü sabit boyutlu bir diziye kopyalayın ve ardından dizi üzerinde yineleyin.

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
