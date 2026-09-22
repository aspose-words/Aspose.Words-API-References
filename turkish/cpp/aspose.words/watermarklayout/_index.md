---
title: "Aspose::Words::WatermarkLayout enum"
linktitle: "WatermarkLayout"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::WatermarkLayout enum. Filigranın merkeze göre düzenini C++'da tanımlar."
type: docs
weight: 130000
url: /tr/cpp/aspose.words/watermarklayout/
---
## WatermarkLayout enum


Filigranın merkeze göre düzenini tanımlar.

```cpp
enum class WatermarkLayout
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| Yatay | 0 | Yatay filigran düzeni. 0 derece dönüşe karşılık gelir. |
| Diyagonal | 315 | Diyagonal filigran düzeni. 315 derece dönüşe karşılık gelir. |


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
