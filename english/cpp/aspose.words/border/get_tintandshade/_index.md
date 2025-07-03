---
title: Aspose::Words::Border::get_TintAndShade method
linktitle: get_TintAndShade
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Border::get_TintAndShade method. Gets or sets a double value that lightens or darkens a color in C++.'
type: docs
weight: 11000
url: /cpp/aspose.words/border/get_tintandshade/
---
## Border::get_TintAndShade method


Gets or sets a double value that lightens or darkens a color.

```cpp
double Aspose::Words::Border::get_TintAndShade()
```

## Remarks


The allowed values are in the range from -1 (the darkest) to 1 (the lightest) for this property. Zero (0) is neutral.

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

* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
