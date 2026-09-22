---
title: "Aspose::Words::Border::get_TintAndShade metodu"
linktitle: "get_TintAndShade"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Border::get_TintAndShade metodu. C++'de bir rengi aydınlatan veya karartan çift bir değeri alır veya ayarlar."
type: docs
weight: 11000
url: /tr/cpp/aspose.words/border/get_tintandshade/
---
## Border::get_TintAndShade method


Bir rengi açan veya karartan çift bir değeri alır veya ayarlar.

```cpp
double Aspose::Words::Border::get_TintAndShade()
```

## Açıklamalar


Bu özellik için izin verilen değerler -1 (en karanlık) ile 1 (en aydınlık) arasında değişir. Sıfır (0) nötrdür.

## Örnekler



Üst kenarlıklı bir paragrafın nasıl ekleneceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Border> topBorder = builder->get_ParagraphFormat()->get_Borders()->get_Top();
topBorder->set_LineWidth(4.0);
topBorder->set_LineStyle(Aspose::Words::LineStyle::DashSmallGap);
// ThemeColor yalnızca LineWidth veya LineStyle ayarlandığında ayarlayın.
topBorder->set_ThemeColor(Aspose::Words::Themes::ThemeColor::Accent1);
topBorder->set_TintAndShade(0.25);

builder->Writeln(u"Text with a top border.");

doc->Save(get_ArtifactsDir() + u"Border.ParagraphTopBorder.docx");
```

## Ayrıca Bakınız

* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
