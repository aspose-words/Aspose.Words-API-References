---
title: "Aspose::Words::TextWatermarkOptions::get_FontSize yöntemi"
linktitle: "get_FontSize"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::TextWatermarkOptions::get_FontSize yöntemi. Bir yazı tipi boyutunu alır veya ayarlar. Varsayılan değer C++'ta 0 - auto'tur."
type: docs
weight: 5000
url: /tr/cpp/aspose.words/textwatermarkoptions/get_fontsize/
---
## TextWatermarkOptions::get_FontSize method


Yazı tipi boyutunu alır veya ayarlar. Varsayılan değer 0 - otomatik.

```cpp
float Aspose::Words::TextWatermarkOptions::get_FontSize() const
```

## Açıklamalar


Geçerli değerler 0 ile 65,5 arasında (her iki uç dahil).

Otomatik yazı tipi boyutu, filigranın sayfa kenar boşluklarına göre maksimum genişliğe ve maksimum yüksekliğe ölçekleneceği anlamına gelir.

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
