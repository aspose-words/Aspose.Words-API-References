---
title: Aspose::Words::Drawing::Fill::set_ForeTintAndShade method
linktitle: set_ForeTintAndShade
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Fill::set_ForeTintAndShade method. Sets a double value that lightens or darkens the foreground color in C++.'
type: docs
weight: 73000
url: /cpp/aspose.words.drawing/fill/set_foretintandshade/
---
## Fill::set_ForeTintAndShade method


Sets a double value that lightens or darkens the foreground color.

```cpp
void Aspose::Words::Drawing::Fill::set_ForeTintAndShade(double value)
```

## Remarks


The allowed values are in the range from -1 (the darkest) to 1 (the lightest) for this property.

Zero (0) is neutral.
## Examples


Shows how to manage lightening and darkening foreground font color.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Big document.docx"));

System::SharedPtr<Aspose::Words::Drawing::Fill> textFill = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Font()->get_Fill();
textFill->set_ForeThemeColor(ThemeColor::Accent1);
if (textFill->get_ForeTintAndShade() == 0)
{
    textFill->set_ForeTintAndShade(0.5);
}

doc->Save(get_ArtifactsDir() + u"Shape.FillTintAndShade.docx");
```
## Exceptions

* **ArgumentOutOfRangeException** - Throw if set this property to a value less than -1 or more than 1.

## See Also

* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
