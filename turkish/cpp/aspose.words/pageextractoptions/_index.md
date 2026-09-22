---
title: "Aspose::Words::PageExtractOptions sınıfı"
linktitle: "PageExtractOptions"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::PageExtractOptions sınıfı. C++'ta belge sayfası çıkarma için seçenekleri belirtmeye izin verir."
type: docs
weight: 45500
url: /tr/cpp/aspose.words/pageextractoptions/
---
## PageExtractOptions class


Belge sayfası çıkarma için seçenekleri belirtmeye izin verir.

```cpp
class PageExtractOptions : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_UnlinkPagesNumberFields](./get_unlinkpagesnumberfields/)() const | Sonuç belgesindeki NUMPAGES alanlarının gerçek sonuç değerleriyle değiştirilip değiştirilmeyeceğini belirtir. Varsayılan değer **true**'dır. |
| [get_UpdatePageStartingNumber](./get_updatepagestartingnumber/)() const | Sonuç belgesindeki başlangıç sayfa numarasının güncellenip güncellenmeyeceğini belirtir. Varsayılan değer **true**'dır. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [PageExtractOptions](./pageextractoptions/)() |  |
| [set_UnlinkPagesNumberFields](./set_unlinkpagesnumberfields/)(bool) | Ayarlayıcı: [Aspose::Words::PageExtractOptions::get_UnlinkPagesNumberFields](./get_unlinkpagesnumberfields/). |
| [set_UpdatePageStartingNumber](./set_updatepagestartingnumber/)(bool) | Ayarlayıcı: [Aspose::Words::PageExtractOptions::get_UpdatePageStartingNumber](./get_updatepagestartingnumber/). |
| static [Type](./type/)() |  |

## Örnekler



İlk sayfa numaralandırmasını sıfırlamayı ve NUMPAGE alanını kaydetmeyi göster.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Page fields.docx");

// Varsayılan davranış:
// Çıkarılan sayfa numaralandırması, orijinal belgede olduğu gibi, sanki MS Word'de "Print 2 pages" seçmiş gibi aynı kalır.
// Başlangıç sayfası 2 olarak ayarlanacak ve sayfa sayısını gösteren alan kaldırılacak
// ve sayfa sayısına eşit sabit bir değerle değiştirilecek.
System::SharedPtr<Aspose::Words::Document> extractedDoc1 = doc->ExtractPages(1, 1);
extractedDoc1->Save(get_ArtifactsDir() + u"Document.ExtractPagesWithOptions.Default.docx");

// Değiştirilmiş davranış:
// Çıkarılan sayfa numaralandırması sıfırlanır ve yeni bir tane başlar,
// sanki ikinci sayfanın içeriğini kopyalayıp yeni bir belgeye yapıştırmış gibi.
// Başlangıç sayfası 1 olarak ayarlanacak ve sayfa sayısını gösteren alan değişmeden bırakılacak
// ve mevcut sayfa sayısını gösterecek.
auto extractOptions = System::MakeObject<Aspose::Words::PageExtractOptions>();
extractOptions->set_UpdatePageStartingNumber(false);
extractOptions->set_UnlinkPagesNumberFields(false);
System::SharedPtr<Aspose::Words::Document> extractedDoc2 = doc->ExtractPages(1, 1, extractOptions);
extractedDoc2->Save(get_ArtifactsDir() + u"Document.ExtractPagesWithOptions.Options.docx");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
