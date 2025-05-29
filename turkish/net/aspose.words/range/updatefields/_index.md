---
title: Range.UpdateFields
linktitle: UpdateFields
articleTitle: UpdateFields
second_title: .NET için Aspose.Words
description: Range UpdateFields yöntemiyle belgelerinizi zahmetsizce geliştirin, alan değerlerini hızlı ve etkili bir şekilde güncelleyerek doğruluğu artırın.
type: docs
weight: 130
url: /tr/net/aspose.words/range/updatefields/
---
## Range.UpdateFields method

Bu aralıktaki belge alanlarının değerlerini günceller.

```csharp
public void UpdateFields()
```

## Notlar

Bir belgeyi açtığınızda, değiştirdiğinizde ve kaydettiğinizde, Aspose.Words alanları otomatik olarak güncellemez, olduğu gibi korur. Bu nedenle, document 'yi programlı olarak değiştirdiyseniz ve kaydedilen belgede doğru (hesaplanan) alan değerlerinin göründüğünden emin olmak istiyorsanız, genellikle kaydetmeden önce bu yöntemi çağırmak istersiniz.

Bir posta birleştirme işlemini gerçekleştirdikten sonra alanları güncellemeye gerek yoktur, çünkü posta birleştirme bir tür update alanıdır ve belgedeki tüm alanları otomatik olarak günceller.

Bu yöntem tüm alan türlerini güncellemez. Desteklenen alan türlerinin ayrıntılı listesi için Programcı Kılavuzu'na bakın.

Bu yöntem, sayfa düzeni algoritmalarıyla ilgili alanları (örneğin PAGE, PAGES, PAGEREF) güncellemez. Sayfa düzeniyle ilgili alanlar, bir belgeyi görüntülediğinizde veya çağırdığınızda güncellenir.[`UpdatePageLayout`](../../document/updatepagelayout/).

Tüm belgedeki alanları güncellemek için şunu kullanın:[`UpdateFields`](../../document/updatefields/).

## Örnekler

Bir aralıktaki tüm alanların nasıl güncelleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" DOCPROPERTY Category");
builder.InsertBreak(BreakType.SectionBreakEvenPage);
builder.InsertField(" DOCPROPERTY Category");

// Yukarıdaki DOCPROPERTY alanları bu yerleşik belge özelliğinin değerini gösterecektir.
doc.BuiltInDocumentProperties.Category = "MyCategory";

// Bir belge özelliğinin değerini güncellersek, bunu görüntülemek için tüm DOCPROPERTY alanlarını güncellememiz gerekir.
Assert.AreEqual(string.Empty, doc.Range.Fields[0].Result);
Assert.AreEqual(string.Empty, doc.Range.Fields[1].Result);

// İlk bölümün aralığındaki tüm alanları güncelle.
doc.FirstSection.Range.UpdateFields();

Assert.AreEqual("MyCategory", doc.Range.Fields[0].Result);
Assert.AreEqual(string.Empty, doc.Range.Fields[1].Result);
```

### Ayrıca bakınız

* class [Range](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
