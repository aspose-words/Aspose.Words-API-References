---
title: NodeCollection.Contains
linktitle: Contains
articleTitle: Contains
second_title: .NET için Aspose.Words
description: NodeCollection Contains yönteminin koleksiyonunuzda bir düğümün bulunup bulunmadığını nasıl etkili bir şekilde kontrol ettiğini ve veri yönetimi yeteneklerinizi nasıl geliştirdiğini keşfedin.
type: docs
weight: 50
url: /tr/net/aspose.words/nodecollection/contains/
---
## NodeCollection.Contains method

Bir düğümün koleksiyonda olup olmadığını belirler.

```csharp
public bool Contains(Node node)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| node | Node | Bulunması gereken düğüm. |

### Geri dönüş değeri

`doğru`eğer öğe koleksiyonda bulunursa; aksi takdirde,`YANLIŞ`.

## Notlar

Bu yöntem doğrusal bir arama gerçekleştirir; bu nedenle, ortalama yürütme süresi şuna orantılıdır:[`Count`](../count/).

## Örnekler

NodeCollection ile nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// DocumentBuilder kullanarak çalıştırmalar ekleyerek belgeye metin ekleyin.
builder.Write("Run 1. ");
builder.Write("Run 2. ");

// "Write" yönteminin her çağrılması yeni bir Çalıştırma oluşturur,
// bu daha sonra ana Paragrafın RunCollection'ında görünür.
RunCollection runs = doc.FirstSection.Body.FirstParagraph.Runs;

Assert.AreEqual(2, runs.Count);

// RunCollection'a manuel olarak da bir düğüm ekleyebiliriz.
Run newRun = new Run(doc, "Run 3. ");
runs.Insert(3, newRun);

Assert.True(runs.Contains(newRun));
Assert.AreEqual("Run 1. Run 2. Run 3.", doc.GetText().Trim());

// Tek tek çalışmalara erişin ve bunları kaldırarak metinlerini belgeden kaldırın.
Run run = runs[1];
runs.Remove(run);

Assert.AreEqual("Run 1. Run 3.", doc.GetText().Trim());
Assert.NotNull(run);
Assert.False(runs.Contains(run));
```

### Ayrıca bakınız

* class [Node](../../node/)
* class [NodeCollection](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
