---
title: "Aspose::Words::WatermarkType enum"
linktitle: "WatermarkType"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::WatermarkType enum. C++'da filigran tipini belirtir."
type: docs
weight: 131000
url: /tr/cpp/aspose.words/watermarktype/
---
## WatermarkType enum


Filigran tipini belirtir.

```cpp
enum class WatermarkType
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| Metin | 0 | Metnin bir filigran olarak kullanılacağını gösterir. Böyle bir filigran, bir WordArt nesnesine karşılık gelir. |
| Image | 1 | Görselin bir filigran olarak kullanılacağını gösterir. Böyle bir filigran, görsel içeren bir şekle karşılık gelir. |
| None | 2 | Filigranın ayarlanmadığını gösterir. |


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
