---
title: "Aspose::Words::Saving::PageSet::PageSet yapıcı"
linktitle: "PageSet"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::PageSet::PageSet yapıcı. C++'ta kesin sayfa indekslerine dayalı bir sayfa seti oluşturur."
type: docs
weight: 5000
url: /tr/cpp/aspose.words.saving/pageset/pageset/
---
## PageSet::PageSet(const System::ArrayPtr\<int32_t\>\&) constructor


Tam sayfa indekslerine dayalı bir sayfa kümesi oluşturur.

```cpp
Aspose::Words::Saving::PageSet::PageSet(const System::ArrayPtr<int32_t> &pages)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| sayfalar | const System::ArrayPtr\<int32_t\>\& | Sayfaların sıfır tabanlı indeksleri. |

## Örnekler



Tam sayfa indekslerine göre sayfaların nasıl çıkarılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Belgeye beş sayfa ekleyin.
for (int32_t i = 1; i < 6; i++)
{
    builder->Write(System::String(u"Page ") + i);
    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
}

// \"XpsSaveOptions\" nesnesi oluşturun, bunu belgenin \"Save\" metoduna aktarabiliriz.
// bu yöntemin belgeyi .XPS'ye nasıl dönüştürdüğünü değiştirmek için.
auto xpsOptions = System::MakeObject<Aspose::Words::Saving::XpsSaveOptions>();

// \"PageSet\" özelliğini kullanarak belgenin bir dizi sayfasını çıktı XPS'ye kaydetmek için seçin.
// Bu durumda, sıfır tabanlı indeks kullanarak yalnızca üç sayfa seçeceğiz: sayfa 1, sayfa 2 ve sayfa 4.
xpsOptions->set_PageSet(System::MakeObject<Aspose::Words::Saving::PageSet>(System::MakeArray<int32_t>({0, 1, 3})));

doc->Save(get_ArtifactsDir() + u"XpsSaveOptions.ExportExactPages.xps", xpsOptions);
```

## Ayrıca Bakınız

* Class [PageSet](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
## PageSet::PageSet(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Saving::PageRange\>\>\&) constructor


Aralıklara dayalı bir sayfa kümesi oluşturur.

```cpp
Aspose::Words::Saving::PageSet::PageSet(const System::ArrayPtr<System::SharedPtr<Aspose::Words::Saving::PageRange>> &ranges)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| aralıklar | const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Saving::PageRange\>\>\& | Sayfa aralıklarının dizisi. |

## Örnekler



Tam sayfa aralıklarına dayalı olarak sayfaları nasıl çıkaracağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

auto imageOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Tiff);
auto pageSet = System::MakeObject<Aspose::Words::Saving::PageSet>(System::MakeArray<System::SharedPtr<Aspose::Words::Saving::PageRange>>({System::MakeObject<Aspose::Words::Saving::PageRange>(1, 1), System::MakeObject<Aspose::Words::Saving::PageRange>(2, 3), System::MakeObject<Aspose::Words::Saving::PageRange>(1, 3), System::MakeObject<Aspose::Words::Saving::PageRange>(2, 4), System::MakeObject<Aspose::Words::Saving::PageRange>(1, 1)}));

imageOptions->set_PageSet(pageSet);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.ExportVariousPageRanges.tiff", imageOptions);
```

## Ayrıca Bakınız

* Class [PageRange](../../pagerange/)
* Class [PageSet](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
## PageSet::PageSet(int32_t) constructor


Tam sayfa indeksine dayalı tek sayfalık bir küme oluşturur.

```cpp
Aspose::Words::Saving::PageSet::PageSet(int32_t page)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| sayfa | int32_t | Sayfanın sıfır tabanlı indeksi. |

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

* Class [PageSet](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
