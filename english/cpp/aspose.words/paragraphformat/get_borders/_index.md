---
title: Aspose::Words::ParagraphFormat::get_Borders method
linktitle: get_Borders
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::ParagraphFormat::get_Borders method. Gets collection of borders of the paragraph in C++.'
type: docs
weight: 7000
url: /cpp/aspose.words/paragraphformat/get_borders/
---
## ParagraphFormat::get_Borders method


Gets collection of borders of the paragraph.

```cpp
System::SharedPtr<Aspose::Words::BorderCollection> Aspose::Words::ParagraphFormat::get_Borders()
```


## Examples



Shows how to insert a paragraph with a top border. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Border> topBorder = builder->get_ParagraphFormat()->get_Borders()->get_Top();
topBorder->set_LineWidth(4.0);
topBorder->set_LineStyle(Aspose::Words::LineStyle::DashSmallGap);
// Set ThemeColor only when LineWidth or LineStyle setted.
topBorder->set_ThemeColor(Aspose::Words::Themes::ThemeColor::Accent1);
topBorder->set_TintAndShade(0.25);

builder->Writeln(u"Text with a top border.");

doc->Save(get_ArtifactsDir() + u"Border.ParagraphTopBorder.docx");
```

## See Also

* Class [BorderCollection](../../bordercollection/)
* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
