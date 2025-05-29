---
title: NodeCollection.Insert
linktitle: Insert
articleTitle: Insert
second_title: .NET için Aspose.Words
description: Basitleştirilmiş Ekleme yöntemimizle NodeCollection'ınıza herhangi bir dizinde zahmetsizce düğümler ekleyin. Veri yönetiminizi bugün geliştirin!
type: docs
weight: 80
url: /tr/net/aspose.words/nodecollection/insert/
---
## NodeCollection.Insert method

Belirtilen dizinde koleksiyona bir düğüm ekler.

```csharp
public void Insert(int index, Node node)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| index | Int32 | Düğümün sıfırdan başlayan indeksi. Negatif indekslere izin verilir ve listenin sonundan erişimi belirtir. Örneğin -1 son düğüm anlamına gelir, -2 sondan bir önceki düğüm anlamına gelir, vb. |
| node | Node | Eklenecek düğüm. |

### istisnalar

| istisna | şart |
| --- | --- |
| NotSupportedException | The[`NodeCollection`](../) "derin" bir koleksiyondur. |

## Notlar

Düğüm, koleksiyonun oluşturulduğu düğüm nesnesine bir çocuk olarak eklenir.

Eğer endeks eşit veya daha büyükse[`Count`](../count/), düğüm koleksiyonun sonuna eklenir.

Eğer endeks negatif ise ve mutlak değeri 'den büyükse[`Count`](../count/), düğüm koleksiyonun sonuna eklenir.

Eklenen düğüm başka bir belgeden oluşturulduysa, kullanmalısınız[`ImportNode`](../../documentbase/importnode/) Düğümü geçerli belgeye aktarmak için. Daha sonra içe aktarılan düğüm geçerli belgeye eklenebilir.

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
