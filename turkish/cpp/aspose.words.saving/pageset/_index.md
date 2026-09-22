---
title: "Aspose::Words::Saving::PageSet sınıfı"
linktitle: "PageSet"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::PageSet sınıfı. Rastgele bir sayfa kümesini tanımlar. Daha fazla bilgi için C++'taki dokümantasyon makalesini ziyaret edin."
type: docs
weight: 20000
url: /tr/cpp/aspose.words.saving/pageset/
---
## PageSet class


Rastgele bir sayfa kümesini tanımlar. Daha fazla bilgi için, [Belgelerle Programlama](https://docs.aspose.com/words/cpp/programming-with-documents/) dokümantasyon makalesini ziyaret edin.

```cpp
class PageSet : public System::Collections::Generic::IEnumerable<int32_t>
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| static [get_All](./get_all/)() | Belgenin tüm sayfalarını orijinal sıralarında içeren bir küme alır. |
| static [get_Even](./get_even/)() | Belgenin tüm çift sayfalarını orijinal sıralarında içeren bir küme alır. |
| static [get_Odd](./get_odd/)() | Belgenin tüm tek sayfalarını orijinal sıralarında içeren bir küme alır. |
| [GetEnumerator](./getenumerator/)() override |  |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [PageSet](./pageset/)(int32_t) | Tam sayfa indeksine dayalı tek sayfalık bir küme oluşturur. |
| [PageSet](./pageset/)(const System::ArrayPtr\<int32_t\>\&) | Tam sayfa indekslerine dayalı bir sayfa kümesi oluşturur. |
| [PageSet](./pageset/)(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Saving::PageRange\>\>\&) | Aralıklara dayalı bir sayfa kümesi oluşturur. |
| static [Type](./type/)() |  |

## Örnekler



Bir belgeden bir sayfayı JPEG görüntüsüne nasıl render edeceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 2.");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 3.");

// Belgenin "Save" yöntemine geçirebileceğimiz bir "ImageSaveOptions" nesnesi oluşturun
// Bu yöntemin belgeyi bir görüntüye render etme şeklini değiştirmek için
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);
// İkinci sayfayı seçmek için "PageSet" değerini "1" olarak ayarlayın
// belgeyi render etmeye başlayacağınız sıfır tabanlı indeks
options->set_PageSet(System::MakeObject<Aspose::Words::Saving::PageSet>(1));

// Belgeyi JPEG formatında kaydettiğimizde, Aspose.Words yalnızca bir sayfayı render eder.
// Bu görüntü, ikinci sayfadan başlayan bir sayfa içerir,
// ki bu da orijinal belgenin sadece ikinci sayfasıdır.
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.OnePage.jpg", options);
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
