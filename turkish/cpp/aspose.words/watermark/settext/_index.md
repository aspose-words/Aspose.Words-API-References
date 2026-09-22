---
title: "Aspose::Words::Watermark::SetText yöntemi"
linktitle: "SetText"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Watermark::SetText yöntemi. Belgeye metin filigranı ekler (C++)."
type: docs
weight: 7000
url: /tr/cpp/aspose.words/watermark/settext/
---
## Watermark::SetText(const System::String\&) method


Belgeye metin filigranı ekler.

```cpp
void Aspose::Words::Watermark::SetText(const System::String &text)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| metin | const System::String\& | Filigran olarak görüntülenen metin. |

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

* Class [Watermark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Watermark::SetText(const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) method


Belgeye metin filigranı ekler.

```cpp
void Aspose::Words::Watermark::SetText(const System::String &text, const System::SharedPtr<Aspose::Words::TextWatermarkOptions> &options)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| metin | const System::String\& | Filigran olarak görüntülenen metin. |
| seçenekler | const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\& | Metin filigranı için ek seçenekleri tanımlar. |

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

* Class [TextWatermarkOptions](../../textwatermarkoptions/)
* Class [Watermark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
