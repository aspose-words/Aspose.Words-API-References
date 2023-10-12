---
title: NodeCollection.Insert
second_title: Aspose.Words for .NET API Referansı
description: NodeCollection yöntem. Belirtilen dizindeki koleksiyona bir düğüm ekler.
type: docs
weight: 80
url: /tr/net/aspose.words/nodecollection/insert/
---
## NodeCollection.Insert method

Belirtilen dizindeki koleksiyona bir düğüm ekler.

```csharp
public void Insert(int index, Node node)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| index | Int32 | Düğümün sıfır tabanlı dizini. Negatif dizinlere izin verilir ve listenin arkasından erişimi belirtir. Örneğin -1 son düğüm anlamına gelir, -2 sondan önceki ikinci anlamına gelir ve bu şekilde devam eder. |
| node | Node | Eklenecek düğüm. |

### istisnalar

| istisna | şart |
| --- | --- |
| NotSupportedException | [`NodeCollection`](../) "derin" bir koleksiyondur. |

### Notlar

Düğüm, koleksiyonun oluşturulduğu düğüm nesnesine alt öğe olarak eklenir.

Endeksin eşit veya büyük olması durumunda[`Count`](../count/)düğüm koleksiyonun sonuna eklenir.

Endeks negatifse ve mutlak değeri şundan büyükse:[`Count`](../count/)düğüm koleksiyonun sonuna eklenir.

Eklenen düğüm başka bir belgeden oluşturulmuşsa kullanmalısınız[`ImportNode`](../../documentbase/importnode/) Düğümü geçerli belgeye aktarmak için. İçe aktarılan düğüm daha sonra geçerli belgeye eklenebilir.

### Örnekler

NodeCollection ile nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// DocumentBuilder kullanarak Çalıştırmalar ekleyerek belgeye metin ekleyin.
builder.Write("Run 1. ");
builder.Write("Run 2. ");

// "Write" yönteminin her çağrılması yeni bir Çalıştırma oluşturur,
// bu daha sonra ana Paragrafın RunCollection'ında görünür.
RunCollection runs = doc.FirstSection.Body.FirstParagraph.Runs;

Assert.AreEqual(2, runs.Count);

// RunCollection'a manuel olarak da düğüm ekleyebiliriz.
Run newRun = new Run(doc, "Run 3. ");
runs.Insert(3, newRun);

Assert.True(runs.Contains(newRun));
Assert.AreEqual("Run 1. Run 2. Run 3.", doc.GetText().Trim());

// Metinlerini belgeden kaldırmak için bireysel çalıştırmalara erişin ve bunları kaldırın.
Run run = runs[1];
runs.Remove(run);

Assert.AreEqual("Run 1. Run 3.", doc.GetText().Trim());
Assert.NotNull(run);
Assert.False(runs.Contains(run));
```

### Ayrıca bakınız

* class [Node](../../node/)
* class [NodeCollection](../)
* ad alanı [Aspose.Words](../../nodecollection/)
* toplantı [Aspose.Words](../../../)


