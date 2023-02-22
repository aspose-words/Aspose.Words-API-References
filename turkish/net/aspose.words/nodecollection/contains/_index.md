---
title: NodeCollection.Contains
second_title: Aspose.Words for .NET API Referansı
description: NodeCollection yöntem. Koleksiyonda bir düğüm olup olmadığını belirler.
type: docs
weight: 50
url: /tr/net/aspose.words/nodecollection/contains/
---
## NodeCollection.Contains method

Koleksiyonda bir düğüm olup olmadığını belirler.

```csharp
public bool Contains(Node node)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| node | Node | Bulunacak düğüm. |

### Geri dönüş değeri

Koleksiyonda öğe bulunursa doğru; aksi halde yanlış.

### Notlar

Bu yöntem doğrusal bir arama gerçekleştirir; bu nedenle, ortalama yürütme süresi Count ile orantılıdır.

### Örnekler

NodeCollection ile nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// DocumentBuilder kullanarak Çalıştırmalar ekleyerek belgeye metin ekleyin.
builder.Write("Run 1. ");
builder.Write("Run 2. ");

// "Write" yönteminin her çağrısı yeni bir Run oluşturur,
// daha sonra üst Paragrafın RunCollection'ında görünür.
RunCollection runs = doc.FirstSection.Body.FirstParagraph.Runs;

Assert.AreEqual(2, runs.Count);

// RunCollection'a manuel olarak da bir düğüm ekleyebiliriz.
Run newRun = new Run(doc, "Run 3. ");
runs.Insert(3, newRun);

Assert.True(runs.Contains(newRun));
Assert.AreEqual("Run 1. Run 2. Run 3.", doc.GetText().Trim());

// Tek tek çalıştırmalara erişin ve metinlerini belgeden kaldırmak için bunları kaldırın.
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


