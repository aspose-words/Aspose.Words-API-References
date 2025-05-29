---
title: Document.AcceptAllRevisions
linktitle: AcceptAllRevisions
articleTitle: AcceptAllRevisions
second_title: .NET için Aspose.Words
description: AcceptAllRevisions yöntemiyle düzenleme sürecinizi kolaylaştırın; belgenizdeki tüm izlenen değişiklikleri zahmetsizce kabul ederek son halini kusursuz hale getirin.
type: docs
weight: 540
url: /tr/net/aspose.words/document/acceptallrevisions/
---
## Document.AcceptAllRevisions method

Belgedeki tüm izlenen değişiklikleri kabul eder.

```csharp
public void AcceptAllRevisions()
```

## Notlar

Bu yöntem bir kısayoldur[`AcceptAll`](../../revisioncollection/acceptall/).

## Örnekler

Belgedeki tüm izleme değişikliklerinin nasıl kabul edileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Değişiklikleri izlerken belgeyi düzenleyerek birkaç düzeltme oluşturun.
doc.StartTrackRevisions("John Doe");
builder.Write("Hello world! ");
builder.Write("Hello again! ");
builder.Write("This is another revision.");
doc.StopTrackRevisions();

Assert.AreEqual(3, doc.Revisions.Count);

// Her revizyonu tekrar tekrar inceleyebilir ve onu belgemizin bir parçası olarak kabul edebilir veya reddedebiliriz.
// Her revizyonu kabul etmek istediğimizi biliyorsak, bunu bu metodu çağırarak daha basit bir şekilde yapabiliriz.
doc.AcceptAllRevisions();

Assert.AreEqual(0, doc.Revisions.Count);
Assert.AreEqual("Hello world! Hello again! This is another revision.", doc.GetText().Trim());
```

### Ayrıca bakınız

* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
