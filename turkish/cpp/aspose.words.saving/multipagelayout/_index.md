---
title: "Aspose::Words::Saving::MultiPageLayout class"
linktitle: "MultiPageLayout"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::MultiPageLayout class. C++'ta birden çok sayfanın tek bir çıktıya işlenmesi için bir yerleşim tanımlar."
type: docs
weight: 14500
url: /tr/cpp/aspose.words.saving/multipagelayout/
---
## MultiPageLayout class


Birden fazla sayfayı tek bir çıktıya render etmek için bir düzen tanımlar.

```cpp
class MultiPageLayout : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_BackColor](./get_backcolor/)() | Çıktının arka plan rengini alır. Varsayılan **Empty**. |
| [get_BorderColor](./get_bordercolor/)() | Sayfaların kenarlık rengini alır. Varsayılan **Empty**. |
| [get_BorderWidth](./get_borderwidth/)() const | Sayfaların kenarlık genişliğini alır. Varsayılan 0. |
| [GetType](./gettype/)() const override |  |
| static [Grid](./grid/)(int32_t, float, float) | Sayfaların soldan sağa, üstten alta, belirtilen sütun sayısıyla bir ızgara içinde işlendiği bir yerleşim oluşturur. |
| static [Horizontal](./horizontal/)(float) | Belirtilen tüm sayfaların yan yana, soldan sağa, tek bir çıktıda yatay olarak işlendiği bir yerleşim oluşturur. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_BackColor](./set_backcolor/)(System::Drawing::Color) | Çıktının arka plan rengini ayarlar. Varsayılan **Empty**. |
| [set_BorderColor](./set_bordercolor/)(System::Drawing::Color) | Sayfaların kenarlık rengini ayarlar. Varsayılan **Empty**. |
| [set_BorderWidth](./set_borderwidth/)(float) | Sayfaların kenarlık genişliğini ayarlar. Varsayılan 0. |
| static [SinglePage](./singlepage/)() | Belirtilen sayfalardan yalnızca ilkini işleyen bir yerleşim oluşturur. |
| static [TiffFrames](./tiffframes/)() | Her sayfanın çok çerçeveli bir TIFF görüntüsünde ayrı bir çerçeve olarak işlendiği bir yerleşim oluşturur. Yalnızca TIFF görüntü formatları için geçerlidir. |
| static [Type](./type/)() |  |
| static [Vertical](./vertical/)(float) | Tüm belirtilen sayfaların dikey olarak birbiri altında tek bir çıktıda render edildiği bir düzen oluşturur. |

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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
