---
title: "Aspose::Words::Border::get_ThemeColor yöntemi"
linktitle: "get_ThemeColor"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Border::get_ThemeColor yöntemi. C++'ta bu Border nesnesiyle ilişkili, uygulanan renk şemasındaki tema rengini alır veya ayarlar."
type: docs
weight: 10000
url: /tr/cpp/aspose.words/border/get_themecolor/
---
## Border::get_ThemeColor method


Uygulanan renk şemasında bu [Border](../) nesnesiyle ilişkili tema rengini alır veya ayarlar.

```cpp
Aspose::Words::Themes::ThemeColor Aspose::Words::Border::get_ThemeColor()
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

* Enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
