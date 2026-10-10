---
title: "Aspose::Words::Saving::ImageSaveOptions::get_PageSet method"
linktitle: "get_PageSet"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::ImageSaveOptions::get_PageSet method. İşlenmek üzere sayfaları alır veya ayarlar. Varsayılan, C++'ta belgede bulunan tüm sayfalardır."
type: docs
weight: 10000
url: /tr/cpp/aspose.words.saving/imagesaveoptions/get_pageset/
---
## ImageSaveOptions::get_PageSet method


Render edilecek sayfaları alır veya ayarlar. Varsayılan, belgede bulunan tüm sayfalardır.

```cpp
System::SharedPtr<Aspose::Words::Saving::PageSet> Aspose::Words::Saving::ImageSaveOptions::get_PageSet()
```

## Açıklamalar


Bu özellik yalnızca belge sayfaları işlenirken etkilidir. Bu özellik şekillerin görüntülere işlenmesi sırasında yok sayılır.

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


Bir belgedeki hangi sayfanın görüntü olarak işleneceğini nasıl belirteceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"Hello world! This is page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"This is page 2.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"This is page 3.");

ASSERT_EQ(3, doc->get_PageCount());

// Belgeyi görüntü olarak kaydettiğimizde, Aspose.Words varsayılan olarak yalnızca ilk sayfayı işler.
// Farklı bir sayfayı işlemek için bir SaveOptions nesnesi geçirebiliriz.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Gif);
// Belgenin her sayfasını ayrı bir görüntü dosyasına işleyin.
for (int32_t i = 1; i <= doc->get_PageCount(); i++)
{
    saveOptions->set_PageSet(System::MakeObject<Aspose::Words::Saving::PageSet>(1));

    doc->Save(get_ArtifactsDir() + System::String::Format(u"ImageSaveOptions.PageIndex.Page {0}.gif", i), saveOptions);
}
```


Bir belgenin her sayfasını ayrı bir TIFF görüntüsüne nasıl render edeceğinizi gösterir.
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
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Tiff);

for (int32_t i = 0; i < doc->get_PageCount(); i++)
{
    // İlk sayfanın numarasını belirten "PageSet" özelliğini şu sayıdan ayarlayın
    // belirtilen sayfadan belgeyi oluşturmaya başlayın.
    options->set_PageSet(System::MakeObject<Aspose::Words::Saving::PageSet>(i));
    // Sayfayı 2325x5325 piksel ve 600 dpi olarak dışa aktar.
    options->set_Resolution(600.0f);
    options->set_ImageSize(System::Drawing::Size(2325, 5325));

    doc->Save(get_ArtifactsDir() + System::String::Format(u"ImageSaveOptions.PageByPage.{0}.tiff", i + 1), options);
}
```


Tam sayfa aralıklarına dayalı olarak sayfaları nasıl çıkaracağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

auto imageOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Tiff);
auto pageSet = System::MakeObject<Aspose::Words::Saving::PageSet>(System::MakeArray<System::SharedPtr<Aspose::Words::Saving::PageRange>>({System::MakeObject<Aspose::Words::Saving::PageRange>(1, 1), System::MakeObject<Aspose::Words::Saving::PageRange>(2, 3), System::MakeObject<Aspose::Words::Saving::PageRange>(1, 3), System::MakeObject<Aspose::Words::Saving::PageRange>(2, 4), System::MakeObject<Aspose::Words::Saving::PageRange>(1, 1)}));

imageOptions->set_PageSet(pageSet);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.ExportVariousPageRanges.tiff", imageOptions);
```

## Ayrıca Bakınız

* Class [PageSet](../../pageset/)
* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
