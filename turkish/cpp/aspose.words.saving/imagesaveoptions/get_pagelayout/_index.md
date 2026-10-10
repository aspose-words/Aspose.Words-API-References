---
title: "Aspose::Words::Saving::ImageSaveOptions::get_PageLayout metodu"
linktitle: "get_PageLayout"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::ImageSaveOptions::get_PageLayout metodu. C++'ta birden çok sayfanın tek bir çıktıya renderlenmesi sırasında kullanılan düzeni alır veya ayarlar."
type: docs
weight: 9500
url: /tr/cpp/aspose.words.saving/imagesaveoptions/get_pagelayout/
---
## ImageSaveOptions::get_PageLayout method


Birden fazla sayfayı tek bir çıktıya render ederken kullanılan düzeni alır veya ayarlar.

```cpp
System::SharedPtr<Aspose::Words::Saving::MultiPageLayout> Aspose::Words::Saving::ImageSaveOptions::get_PageLayout() const
```

## Açıklamalar


Bu özelliği yapılandırmak için [MultiPageLayout](../../multipagelayout/) sınıfının fabrika yöntemlerinden birini kullanın.

[Tiff](../../../aspose.words/saveformat/) için varsayılan değer [TiffFrames](../../multipagelayout/tiffframes/)'dır. Diğer formatlar için varsayılan değer [SinglePage](../../multipagelayout/singlepage/)'dır.

Bu özellik yalnızca aşağıdaki formatlara kaydedilirken etkili olur: [Jpeg](../../../aspose.words/saveformat/), [Gif](../../../aspose.words/saveformat/), [Png](../../../aspose.words/saveformat/), [Bmp](../../../aspose.words/saveformat/), [Tiff](../../../aspose.words/saveformat/), [WebP](../)

## Örnekler



Belgeyi çok sayfalı düzen ayarlarıyla JPG görüntüsü olarak nasıl kaydedeceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);
// Şu öğelerle bir ızgara düzeni kurun:
// - Satır başına 3 sütun.
// - Sayfalar arasında (yatay ve dikey) 10 puan boşluk.
options->set_PageLayout(Aspose::Words::Saving::MultiPageLayout::Grid(3, 10.0f, 10.0f));

// Alternatif düzenler:
// options.PageLayout = MultiPageLayout.Horizontal(10);
// options.PageLayout = MultiPageLayout.Vertical(10);

// Arka planı ve kenarlığı özelleştirin.
options->get_PageLayout()->set_BackColor(System::Drawing::Color::get_LightGray());
options->get_PageLayout()->set_BorderColor(System::Drawing::Color::get_Blue());
options->get_PageLayout()->set_BorderWidth(2.0f);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.GridLayout.jpg", options);
```

## Ayrıca Bakınız

* Class [MultiPageLayout](../../multipagelayout/)
* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
