---
title: "Aspose::Words::Watermark sınıfı"
linktitle: "Filigran"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Watermark sınıfı. Belge filigranı ile çalışmak için sınıfı temsil eder. Daha fazla bilgi için C++'daki dokümantasyon makalesini ziyaret edin."
type: docs
weight: 76000
url: /tr/cpp/aspose.words/watermark/
---
## Watermark class


Belge filigranı ile çalışmak için sınıfı temsil eder. Daha fazla bilgi edinmek için, [Working with Watermark](https://docs.aspose.com/words/cpp/working-with-watermark/) belgeler makalesini ziyaret edin.

```cpp
class Watermark : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_Type](./get_type/)() | Filigran türünü alır. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() | Filigranı kaldırır. |
| [SetImage](./setimage/)(const System::SharedPtr\<System::Drawing::Image\>\&) | Belgeye resim filigranı ekler. |
| [SetImage](./setimage/)(const System::SharedPtr\<System::Drawing::Image\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | Belgeye resim filigranı ekler. |
| [SetImage](./setimage/)(const System::String\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | Belgeye resim filigranı ekler. |
| [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | Belgeye resim filigranı ekler. |
| [SetText](./settext/)(const System::String\&) | Belgeye metin filigranı ekler. |
| [SetText](./settext/)(const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) | Belgeye metin filigranı ekler. |
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
