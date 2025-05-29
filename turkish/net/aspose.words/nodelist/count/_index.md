---
title: NodeList.Count
linktitle: Count
articleTitle: Count
second_title: .NET için Aspose.Words
description: Listenizdeki düğümlerin toplam sayısını kolayca almak için NodeList Count özelliğini keşfedin ve web geliştirme verimliliğinizi artırın.
type: docs
weight: 10
url: /tr/net/aspose.words/nodelist/count/
---
## NodeList.Count property

Listedeki düğüm sayısını alır.

```csharp
public int Count { get; }
```

## Örnekler

Bir NodeList'te gezinmek için XPath'lerin nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// DocumentBuilder ile birkaç düğüm ekle.
builder.Writeln("Hello world!");

builder.StartTable();
builder.InsertCell();
builder.Write("Cell 1");
builder.InsertCell();
builder.Write("Cell 2");
builder.EndTable();

builder.InsertImage(ImageDir + "Logo.jpg");

// Belgemizde üç adet Run düğümü bulunmaktadır.
NodeList nodeList = doc.SelectNodes("//Koşmak");

Assert.AreEqual(3, nodeList.Count);
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Hello world!"));
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Cell 1"));
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Cell 2"));

// Tüm Çalıştırma düğümlerini seçmek için çift eğik çizgi kullanın
// bunlar, eklediğimiz iki hücrenin içindeki çalışmalar olacak olan Tablo düğümünün dolaylı alt öğeleridir.
nodeList = doc.SelectNodes("//Table//Koşmak");

Assert.AreEqual(2, nodeList.Count);
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Cell 1"));
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Cell 2"));

// Tek eğik çizgiler doğrudan alt ilişkileri belirtir,
// çift eğik çizgi kullandığımızda bunu atladık.
Assert.AreEqual(doc.SelectNodes(" //Tablo//Çalıştır"),
    doc.SelectNodes("//Tablo/Satır/Hücre/Paragraf/Çalıştır"));

// Eklediğimiz görseli içeren şekle eriş.
nodeList = doc.SelectNodes("//Şekil");

Assert.AreEqual(1, nodeList.Count);

Shape shape = (Shape)nodeList[0];
Assert.True(shape.HasImage);
```

### Ayrıca bakınız

* class [NodeList](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
