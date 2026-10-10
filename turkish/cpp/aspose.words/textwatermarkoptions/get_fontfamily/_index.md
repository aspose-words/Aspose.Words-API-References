---
title: "Aspose::Words::TextWatermarkOptions::get_FontFamily method"
linktitle: "get_FontFamily"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::TextWatermarkOptions::get_FontFamily yöntemi. Yazı tipi ailesi adını alır veya ayarlar. Varsayılan değer C++'ta \"Calibri\"dır."
type: docs
weight: 4000
url: /tr/cpp/aspose.words/textwatermarkoptions/get_fontfamily/
---
## TextWatermarkOptions::get_FontFamily method


Yazı tipi ailesi adını alır veya ayarlar. Varsayılan değer "Calibri"'dır.

```cpp
System::String Aspose::Words::TextWatermarkOptions::get_FontFamily() const
```


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

* Class [TextWatermarkOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
