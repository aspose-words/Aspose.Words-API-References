---
title: Aspose::Words::Border::set_TintAndShade method
linktitle: set_TintAndShade
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Border::set_TintAndShade method. Sets a double value that lightens or darkens a color in C++.'
type: docs
weight: 21000
url: /cpp/aspose.words/border/set_tintandshade/
---
## Border::set_TintAndShade method


Sets a double value that lightens or darkens a color.

```cpp
void Aspose::Words::Border::set_TintAndShade(double value)
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
topBorder->set_LineStyle(LineStyle::DashSmallGap);
// Set ThemeColor only when LineWidth or LineStyle setted.
topBorder->set_ThemeColor(ThemeColor::Accent1);
topBorder->set_TintAndShade(0.25);

builder->Writeln(u"Text with a top border.");

doc->Save(get_ArtifactsDir() + u"Border.ParagraphTopBorder.docx");
```
## Exceptions

* **ArgumentOutOfRangeException** - Throws if you attempt to set this property to a value less than -1 or more than 1.
* **InvalidOperationException** - Throws if setting this property for Border object with non-theme colors.

## See Also

* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
