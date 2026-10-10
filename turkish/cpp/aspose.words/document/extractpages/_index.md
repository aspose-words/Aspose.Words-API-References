---
title: "Aspose::Words::Document::ExtractPages yöntemi"
linktitle: "ExtractPages"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Document::ExtractPages yöntemi. C++'ta belirtilen sayfa aralığını temsil eden Document nesnesini döndürür."
type: docs
weight: 12000
url: /tr/cpp/aspose.words/document/extractpages/
---
## Document::ExtractPages(int32_t, int32_t) method


Belirtilen sayfa aralığını temsil eden [Document](../) nesnesini döndürür.

```cpp
System::SharedPtr<Aspose::Words::Document> Aspose::Words::Document::ExtractPages(int32_t index, int32_t count)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| index | int32_t | Çıkarılacak ilk sayfanın sıfır tabanlı indeksi. |
| count | int32_t | Çıkarılacak sayfa sayısı. |

## Örnekler



Belgeden belirtilen sayfa aralığını nasıl alacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Layout entities.docx");

doc = doc->ExtractPages(0, 2);

doc->Save(get_ArtifactsDir() + u"Document.ExtractPages.docx");
```


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

* Class [Document](../)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::ExtractPages(int32_t, int32_t, const System::SharedPtr\<Aspose::Words::PageExtractOptions\>\&) method


Belirtilen sayfa aralığını ve verilen sayfa çıkarma seçeneklerini temsil eden [Belge](../) nesnesini döndürür.

```cpp
System::SharedPtr<Aspose::Words::Document> Aspose::Words::Document::ExtractPages(int32_t index, int32_t count, const System::SharedPtr<Aspose::Words::PageExtractOptions> &options)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| index | int32_t | Çıkarılacak ilk sayfanın sıfır tabanlı indeksi. |
| count | int32_t | Çıkarılacak sayfa sayısı. |
| seçenekler | const System::SharedPtr\<Aspose::Words::PageExtractOptions\>\& | Sayfa çıkarma sürecini yönetmek için seçenekler sağlar. |

## Ayrıca Bakınız

* Class [Document](../)
* Class [PageExtractOptions](../../pageextractoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
