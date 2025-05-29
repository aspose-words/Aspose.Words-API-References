---
title: NodeCollection.Remove
linktitle: Remove
articleTitle: Remove
second_title: .NET için Aspose.Words
description: NodeCollection Remove yöntemi ile belgenizden düğümleri zahmetsizce kaldırın, böylece veri yönetiminizi kolaylaştırın ve performansı artırın.
type: docs
weight: 90
url: /tr/net/aspose.words/nodecollection/remove/
---
## NodeCollection.Remove method

Düğümü koleksiyondan ve belgeden kaldırır.

```csharp
public void Remove(Node node)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| node | Node | Kaldırılacak düğüm. |

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
