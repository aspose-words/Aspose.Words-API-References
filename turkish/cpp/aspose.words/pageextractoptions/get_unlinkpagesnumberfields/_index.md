---
title: "Aspose::Words::PageExtractOptions::get_UnlinkPagesNumberFields metodu"
linktitle: "get_UnlinkPagesNumberFields"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::PageExtractOptions::get_UnlinkPagesNumberFields metodu. Sonuç belgesindeki NUMPAGES alanlarının gerçek sonuç değerleriyle değiştirilip değiştirilmeyeceğini belirler. Varsayılan değer C++'ta true'dur."
type: docs
weight: 3000
url: /tr/cpp/aspose.words/pageextractoptions/get_unlinkpagesnumberfields/
---
## PageExtractOptions::get_UnlinkPagesNumberFields method


Sonuç belgesindeki NUMPAGES alanlarının gerçek sonuç değerleriyle değiştirilip değiştirilmeyeceğini belirtir. Varsayılan değer **true**'dır.

```cpp
bool Aspose::Words::PageExtractOptions::get_UnlinkPagesNumberFields() const
```


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

* Class [PageExtractOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
