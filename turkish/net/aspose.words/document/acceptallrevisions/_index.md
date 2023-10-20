---
title: Document.AcceptAllRevisions
linktitle: AcceptAllRevisions
articleTitle: AcceptAllRevisions
second_title: Aspose.Words for .NET
description: Document AcceptAllRevisions yöntem. Belgede izlenen tüm değişiklikleri kabul eder C#'da.
type: docs
weight: 520
url: /tr/net/aspose.words/document/acceptallrevisions/
---
## Document.AcceptAllRevisions method

Belgede izlenen tüm değişiklikleri kabul eder.

```csharp
public void AcceptAllRevisions()
```

## Notlar

Bu yöntem kısa yol[`AcceptAll`](../../revisioncollection/acceptall/).

## Örnekler

Belgedeki tüm izleme değişikliklerinin nasıl kabul edileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Birkaç revizyon oluşturmak için değişiklikleri izlerken belgeyi düzenleyin.
doc.StartTrackRevisions("John Doe");
builder.Write("Hello world! ");
builder.Write("Hello again! "); 
builder.Write("This is another revision.");
doc.StopTrackRevisions();

Assert.AreEqual(3, doc.Revisions.Count);

// Her revizyonu yineleyebilir ve onu belgemizin bir parçası olarak kabul edebilir/reddedebiliriz.
// Her revizyonu kabul etmek istediğimizi biliyorsak, bu yöntemi çağırarak bunu daha basit bir şekilde yapabiliriz.
doc.AcceptAllRevisions();

Assert.AreEqual(0, doc.Revisions.Count);
Assert.AreEqual("Hello world! Hello again! This is another revision.", doc.GetText().Trim());
```

### Ayrıca bakınız

* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
