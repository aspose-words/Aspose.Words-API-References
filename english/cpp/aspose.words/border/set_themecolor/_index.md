---
title: Aspose::Words::Border::set_ThemeColor method
linktitle: set_ThemeColor
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Border::set_ThemeColor method. Sets the theme color in the applied color scheme that is associated with this Border object in C++.'
type: docs
weight: 20000
url: /cpp/aspose.words/border/set_themecolor/
---
## Border::set_ThemeColor method


Sets the theme color in the applied color scheme that is associated with this Border object.

```cpp
void Aspose::Words::Border::set_ThemeColor(Aspose::Words::Themes::ThemeColor value)
```

## Examples


Shows how to insert a paragraph with a top border.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Border> topBorder = builder->get_ParagraphFormat()->get_Borders()->get_Top();
topBorder->set_LineWidth(4.0);
topBorder->set_LineStyle(LineStyle::DashSmallGap);
// Set ThemeColor only when LineWidth or LineStyle setted.
topBorder->set_ThemeColor(ThemeColor::Accent1);
topBorder->set_TintAndShade(0.25);

builder->Writeln(u"Text with a top border.");

doc->Save(get_ArtifactsDir() + u"Border.ParagraphTopBorder.docx");
```
## See Also

* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
