---
title: "Aspose::Words::Font::get_AutoColor yöntemi"
linktitle: "get_AutoColor"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Font::get_AutoColor yöntemi. Metnin (siyah veya beyaz) şu an hesaplanan rengini ''auto color'' için döndürür. Renk ''auto'' değilse C++'ta Color döndürür."
type: docs
weight: 4000
url: /tr/cpp/aspose.words/font/get_autocolor/
---
## Font::get_AutoColor method


Metnin (siyah veya beyaz) şu an hesaplanan rengini 'auto color' için döndürür. Renk 'auto' değilse [Color](../get_color/) döndürür.

```cpp
System::Drawing::Color Aspose::Words::Font::get_AutoColor()
```

## Açıklamalar


'automatic color' olduğunda, metnin gerçek rengi arka plan rengine karşı okunabilir olacak şekilde otomatik olarak hesaplanır. Arka plan rengini değiştirdiğinizde, metin rengi MS Word'de okunabilirliği en üst düzeye çıkarmak için otomatik olarak siyah veya beyaza geçer.

## Örnekler



Arka planın parlaklığına göre metin rengini otomatik olarak seçerek okunabilirliği nasıl artıracağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Bir koşunun Font nesnesi metin rengini belirtmezse, otomatik olarak
// arka plan renginin rengine bağlı olarak siyah veya beyazı seçer.
ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), builder->get_Font()->get_Color().ToArgb());

// Metin için varsayılan renk siyahtır. Arka plan rengi koyuysa, siyah metin görülmesi zor olur.
// Bu sorunu çözmek için AutoColor özelliği bu metni beyaz olarak gösterir.
builder->get_Font()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_DarkBlue());

builder->Writeln(u"The text color automatically chosen for this run is white.");

ASSERT_EQ(System::Drawing::Color::get_White().ToArgb(), doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_Runs()->idx_get(0)->get_Font()->get_AutoColor().ToArgb());

// Arka planı açık bir renge değiştirirsek, siyah daha
// beyazdan daha uygun bir metin rengi olur, böylece otomatik renk onu siyah olarak gösterir.
builder->get_Font()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightBlue());

builder->Writeln(u"The text color automatically chosen for this run is black.");

ASSERT_EQ(System::Drawing::Color::get_Black().ToArgb(), doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1)->get_Runs()->idx_get(0)->get_Font()->get_AutoColor().ToArgb());

doc->Save(get_ArtifactsDir() + u"Font.SetFontAutoColor.docx");
```

## Ayrıca Bakınız

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
