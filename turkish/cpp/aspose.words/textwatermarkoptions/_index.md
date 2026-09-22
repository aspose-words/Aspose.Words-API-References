---
title: "Aspose::Words::TextWatermarkOptions class"
linktitle: "TextWatermarkOptions"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::TextWatermarkOptions sınıfı. Metinle bir filigran eklerken belirtilebilecek seçenekleri içerir. Daha fazla bilgi edinmek için C++'daki dokümantasyon makalesini ziyaret edin."
type: docs
weight: 72000
url: /tr/cpp/aspose.words/textwatermarkoptions/
---
## TextWatermarkOptions class


Metin içeren bir filigran eklerken belirtilebilecek seçenekleri içerir. Daha fazla bilgi edinmek için, [Working with Watermark](https://docs.aspose.com/words/cpp/working-with-watermark/) belgeler makalesini ziyaret edin.

```cpp
class TextWatermarkOptions : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_Color](./get_color/)() const | Yazı tipi rengini alır veya ayarlar. Varsayılan değer **Silver**'dır. |
| [get_FontFamily](./get_fontfamily/)() const | Yazı tipi ailesi adını alır veya ayarlar. Varsayılan değer "Calibri"'dır. |
| [get_FontSize](./get_fontsize/)() const | Yazı tipi boyutunu alır veya ayarlar. Varsayılan değer 0 - otomatik. |
| [get_IsSemitrasparent](./get_issemitrasparent/)() const | Filigranın opaklığından sorumlu bir boolean değeri alır veya ayarlar. Varsayılan değer **true**'dır. |
| [get_Layout](./get_layout/)() const | Filigranın düzenini alır veya ayarlar. Varsayılan değer [Diagonal](../watermarklayout/)'dır. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Color](./set_color/)(System::Drawing::Color) | [Aspose::Words::TextWatermarkOptions::get_Color](./get_color/) için ayarlayıcı. |
| [set_FontFamily](./set_fontfamily/)(const System::String\&) | [Aspose::Words::TextWatermarkOptions::get_FontFamily](./get_fontfamily/) için ayarlayıcı. |
| [set_FontSize](./set_fontsize/)(float) | [Aspose::Words::TextWatermarkOptions::get_FontSize](./get_fontsize/) için ayarlayıcı. |
| [set_IsSemitrasparent](./set_issemitrasparent/)(bool) | [Aspose::Words::TextWatermarkOptions::get_IsSemitrasparent](./get_issemitrasparent/) için ayarlayıcı. |
| [set_Layout](./set_layout/)(Aspose::Words::WatermarkLayout) | [Aspose::Words::TextWatermarkOptions::get_Layout](./get_layout/) için ayarlayıcı. |
| [TextWatermarkOptions](./textwatermarkoptions/)() |  |
| static [Type](./type/)() |  |

## Örnekler



Metin filigranı oluşturmayı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Düz metin filigranı ekleyin.
doc->get_Watermark()->SetText(u"Aspose Watermark");

// Bunu bir filigran olarak kullanarak metin biçimlendirmesini düzenlemek istersek,
// Filigranı oluştururken bir TextWatermarkOptions nesnesi geçirerek bunu yapabiliriz.
auto textWatermarkOptions = System::MakeObject<Aspose::Words::TextWatermarkOptions>();
textWatermarkOptions->set_FontFamily(u"Arial");
textWatermarkOptions->set_FontSize(36.0f);
textWatermarkOptions->set_Color(System::Drawing::Color::get_Black());
textWatermarkOptions->set_Layout(Aspose::Words::WatermarkLayout::Diagonal);
textWatermarkOptions->set_IsSemitrasparent(false);

doc->get_Watermark()->SetText(u"Aspose Watermark", textWatermarkOptions);

doc->Save(get_ArtifactsDir() + u"Document.TextWatermark.docx");

// Bir belgeden bu şekilde bir filigran kaldırabiliriz.
if (doc->get_Watermark()->get_Type() == Aspose::Words::WatermarkType::Text)
{
    doc->get_Watermark()->Remove();
}
```

## Ayrıca Bakınız

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
