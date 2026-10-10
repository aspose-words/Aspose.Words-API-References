---
title: "Aspose::Words::Drawing::Fill::get_ForeTintAndShade yöntemi"
linktitle: "get_ForeTintAndShade"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Fill::get_ForeTintAndShade yöntemi. C++'da ön plan rengini aydınlatan veya karartan bir double değer alır veya ayarlar."
type: docs
weight: 9000
url: /tr/cpp/aspose.words.drawing/fill/get_foretintandshade/
---
## Fill::get_ForeTintAndShade method


Ön plan rengini açan veya karartan bir double değerini alır veya ayarlar.

```cpp
double Aspose::Words::Drawing::Fill::get_ForeTintAndShade()
```

## Açıklamalar


Bu özellik için izin verilen değerler -1 (en karanlık) ile 1 (en açık) arasındadır.

Sıfır (0) nötrdür.

## Örnekler



Ön plan yazı tipinin aydınlatma ve karartma yönetiminin nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");

System::SharedPtr<Aspose::Words::Drawing::Fill> textFill = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Font()->get_Fill();
textFill->set_ForeThemeColor(Aspose::Words::Themes::ThemeColor::Accent1);
if (textFill->get_ForeTintAndShade() == 0)
{
    textFill->set_ForeTintAndShade(0.5);
}

doc->Save(get_ArtifactsDir() + u"Shape.FillTintAndShade.docx");
```

## Ayrıca Bakınız

* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
