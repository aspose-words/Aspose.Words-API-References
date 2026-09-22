---
title: "Aspose::Words::Range::UpdateFields yöntemi"
linktitle: "UpdateFields"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Range::UpdateFields yöntemi. C++'da bu aralıktaki belge alanı değerlerini günceller."
type: docs
weight: 15000
url: /tr/cpp/aspose.words/range/updatefields/
---
## Range::UpdateFields method


Bu aralıktaki belge alanlarının değerlerini günceller.

```cpp
void Aspose::Words::Range::UpdateFields()
```

## Açıklamalar


Bir belgeyi açıp, değiştirip ardından kaydettiğinizde, Aspose.Words alanları otomatik olarak güncellemez, onları aynı tutar. Bu nedenle, belgeyi programlı olarak değiştirdiyseniz ve kaydedilen belgede doğru (hesaplanmış) alan değerlerinin görünmesini sağlamak istiyorsanız, genellikle kaydetmeden önce bu metodu çağırmak istersiniz.

Posta birleştirme işlemi gerçekleştirdikten sonra alanları güncellemenize gerek yoktur, çünkü posta birleştirme bir alan güncellemesi türüdür ve belgedeki tüm alanları otomatik olarak günceller.

Bu metod tüm alan türlerini güncellemez. Desteklenen alan türlerinin ayrıntılı listesi için Programcılar Kılavuzuna bakın.

Bu yöntem, sayfa düzeni algoritmalarıyla (ör. PAGE, PAGES, PAGEREF) ilgili alanları güncellemez. Sayfa düzeniyle ilgili alanlar, bir belgeyi işlediğinizde veya [UpdatePageLayout](../../document/updatepagelayout/) çağırdığınızda güncellenir.

Tüm belgede alanları güncellemek için [UpdateFields](../../document/updatefields/) kullanın.

## Örnekler



Bir aralıktaki tüm alanların nasıl güncelleneceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertField(u" DOCPROPERTY Category");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakEvenPage);
builder->InsertField(u" DOCPROPERTY Category");

// Yukarıdaki DOCPROPERTY alanları bu yerleşik belge özelliğinin değerini gösterecektir.
doc->get_BuiltInDocumentProperties()->set_Category(u"MyCategory");

// Bir belge özelliğinin değerini güncellerseniz, bunu göstermek için tüm DOCPROPERTY alanlarını da güncellemeniz gerekir.
ASSERT_EQ(System::String::Empty, doc->get_Range()->get_Fields()->idx_get(0)->get_Result());
ASSERT_EQ(System::String::Empty, doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

// İlk bölümün aralığındaki tüm alanları güncelleyin.
doc->get_FirstSection()->get_Range()->UpdateFields();

ASSERT_EQ(u"MyCategory", doc->get_Range()->get_Fields()->idx_get(0)->get_Result());
ASSERT_EQ(System::String::Empty, doc->get_Range()->get_Fields()->idx_get(1)->get_Result());
```

## Ayrıca Bakınız

* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
