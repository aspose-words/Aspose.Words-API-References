---
title: "Aspose::Words::ParagraphFormat::get_Borders yöntemi"
linktitle: "get_Borders"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::ParagraphFormat::get_Borders yöntemi. C++'ta paragrafın kenarlık koleksiyonunu alır."
type: docs
weight: 7000
url: /tr/cpp/aspose.words/paragraphformat/get_borders/
---
## ParagraphFormat::get_Borders method


Paragrafın kenarlık koleksiyonunu alır.

```cpp
System::SharedPtr<Aspose::Words::BorderCollection> Aspose::Words::ParagraphFormat::get_Borders()
```


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

* Class [BorderCollection](../../bordercollection/)
* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
