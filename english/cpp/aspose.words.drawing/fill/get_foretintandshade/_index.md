---
title: Aspose::Words::Drawing::Fill::get_ForeTintAndShade method
linktitle: get_ForeTintAndShade
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Fill::get_ForeTintAndShade method. Gets or sets a double value that lightens or darkens the foreground color in C++.'
type: docs
weight: 9000
url: /cpp/aspose.words.drawing/fill/get_foretintandshade/
---
## Fill::get_ForeTintAndShade method


Gets or sets a double value that lightens or darkens the foreground color.

```cpp
double Aspose::Words::Drawing::Fill::get_ForeTintAndShade()
```

## Remarks


The allowed values are in the range from -1 (the darkest) to 1 (the lightest) for this property.

Zero (0) is neutral.

## Examples



Shows how to manage lightening and darkening foreground font color. 
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

## See Also

* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
