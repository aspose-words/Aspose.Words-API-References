---
title: Range.UpdateFields
second_title: Aspose.Words for .NET API Referansı
description: Range yöntem. Bu aralıktaki belge alanlarının değerlerini günceller.
type: docs
weight: 120
url: /tr/net/aspose.words/range/updatefields/
---
## Range.UpdateFields method

Bu aralıktaki belge alanlarının değerlerini günceller.

```csharp
public void UpdateFields()
```

### Notlar

Bir belgeyi açtığınızda, değiştirdiğinizde ve ardından kaydettiğinizde Aspose.Words, alanları otomatik olarak güncellemez, onları olduğu gibi tutar. Bu nedenle, document dosyasını programlı olarak değiştirdiyseniz ve emin olmak istiyorsanız, genellikle kaydetmeden önce bu yöntemi çağırmak istersiniz. kaydedilen belgede uygun (hesaplanan) alan değerleri görünür.

Adres-mektup birleştirmeyi yürüttükten sonra alanları güncellemeye gerek yoktur çünkü adres-mektup birleştirme bir tür update alanıdır ve belgedeki tüm alanları otomatik olarak günceller.

Bu yöntem tüm alan türlerini güncellemez. Desteklenen alan türlerinin ayrıntılı listesi için Programcı Kılavuzu'na bakın.

Bu yöntem, sayfa düzeni algoritmalarıyla ilgili alanları (örn. PAGE, PAGES, PAGEREF) güncellemez. Sayfa düzeniyle ilgili alanlar, bir belgeyi oluşturduğunuzda veya çağrı yaptığınızda güncellenir.[`UpdatePageLayout`](../../document/updatepagelayout/).

Belgenin tamamındaki alanları güncellemek için şunu kullanın:[`UpdateFields`](../../document/updatefields/).

### Örnekler

Bir aralıktaki tüm alanların nasıl güncelleştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" DOCPROPERTY Category");
builder.InsertBreak(BreakType.SectionBreakEvenPage);
builder.InsertField(" DOCPROPERTY Category");

// Yukarıdaki DOCPROPERTY alanları bu yerleşik belge özelliğinin değerini görüntüleyecektir.
doc.BuiltInDocumentProperties.Category = "MyCategory";

// Bir belge özelliğinin değerini güncellersek, onu görüntülemek için tüm DOCPROPERTY alanlarını güncellememiz gerekecektir.
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


