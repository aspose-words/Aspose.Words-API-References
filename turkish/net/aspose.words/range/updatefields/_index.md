---
title: Range.UpdateFields
second_title: Aspose.Words for .NET API Referansı
description: Range yöntem. Bu aralıktaki belge alanlarının değerlerini günceller.
type: docs
weight: 110
url: /tr/net/aspose.words/range/updatefields/
---
## Range.UpdateFields method

Bu aralıktaki belge alanlarının değerlerini günceller.

```csharp
public void UpdateFields()
```

### Notlar

Bir belgeyi açtığınızda, değiştirdiğinizde ve sonra kaydettiğinizde, Aspose.Words alanları otomatik olarak güncellemez, onları olduğu gibi tutar. Bu nedenle, document 'yi programlı olarak değiştirdiyseniz ve emin olmak istiyorsanız, kaydetmeden önce genellikle bu yöntemi çağırmak istersiniz. uygun (hesaplanmış) alan değerleri kaydedilen belgede görünür.

Adres mektup birleştirme yürütüldükten sonra alanları güncellemeye gerek yoktur çünkü adres mektup birleştirme bir tür update alanıdır ve belgedeki tüm alanları otomatik olarak günceller.

Bu yöntem tüm alan türlerini güncellemez. Desteklenen alan türlerinin ayrıntılı listesi için Programcı Kılavuzu'na bakın.

Bu yöntem, sayfa düzeni algoritmalarıyla ilgili alanları güncellemez (örn. PAGE, PAGES, PAGEREF). Bir belge oluşturduğunuzda veya çağırdığınızda sayfa düzeniyle ilgili alanlar güncellenir.[`UpdatePageLayout`](../../document/updatepagelayout/).

Tüm belge kullanımındaki alanları güncellemek için[`UpdateFields`](../../document/updatefields/).

### Örnekler

Bir aralıktaki tüm alanların nasıl güncelleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" DOCPROPERTY Category");
builder.InsertBreak(BreakType.SectionBreakEvenPage);
builder.InsertField(" DOCPROPERTY Category");

// Yukarıdaki DOCPROPERTY alanları, bu yerleşik belge özelliğinin değerini görüntüleyecektir.
doc.BuiltInDocumentProperties.Category = "MyCategory";

// Bir belge özelliğinin değerini güncellersek, onu görüntülemek için tüm DOCPROPERTY alanlarını güncellememiz gerekecek.
Assert.AreEqual(string.Empty, doc.Range.Fields[0].Result);
Assert.AreEqual(string.Empty, doc.Range.Fields[1].Result);

// İlk bölümün aralığındaki tüm alanları güncelleyin.
doc.FirstSection.Range.UpdateFields();

Assert.AreEqual("MyCategory", doc.Range.Fields[0].Result);
Assert.AreEqual(string.Empty, doc.Range.Fields[1].Result);
```

### Ayrıca bakınız

* class [Range](../)
* ad alanı [Aspose.Words](../../range/)
* toplantı [Aspose.Words](../../../)


