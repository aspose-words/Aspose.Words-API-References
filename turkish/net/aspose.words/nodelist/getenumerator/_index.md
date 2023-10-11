---
title: NodeList.GetEnumerator
second_title: Aspose.Words for .NET API Referansı
description: NodeList yöntem. Düğümlerin koleksiyonu üzerinde basit bir foreach stili yinelemesi sağlar.
type: docs
weight: 30
url: /tr/net/aspose.words/nodelist/getenumerator/
---
## NodeList.GetEnumerator method

Düğümlerin koleksiyonu üzerinde basit bir "foreach" stili yinelemesi sağlar.

```csharp
public IEnumerator<Node> GetEnumerator()
```

### Geri dönüş değeri

Bir IEnumerator.

### Örnekler

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
* ad alanı [Aspose.Words](../../nodelist/)
* toplantı [Aspose.Words](../../../)


