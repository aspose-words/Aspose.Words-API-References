---
title: get_AutoColor
second_title: Aspose.Words for C++ API Reference
description: Returns the present calculated color of the text (black or white) to be used for 'auto color'. If the color is not 'auto' then returns Color.
type: docs
weight: 27
url: /cpp/aspose.words/font/get_autocolor/
---
## Font::get_AutoColor method


Returns the present calculated color of the text (black or white) to be used for 'auto color'. If the color is not 'auto' then returns [Color](../get_color/).

```cpp
System::Drawing::Color Aspose::Words::Font::get_AutoColor()
```

## Remarks


When text has 'automatic color', the actual color of text is calculated automatically so that it is readable against the background color. As you change the background color, the text color will automatically switch to black or white in MS Word to maximize legibility.

## Examples



Shows how to improve readability by automatically selecting text color based on the brightness of its background. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// If a run's Font object does not specify text color, it will automatically
// select either black or white depending on the background color's color.
ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), builder->get_Font()->get_Color().ToArgb());

// The default color for text is black. If the color of the background is dark, black text will be difficult to see.
// To solve this problem, the AutoColor property will display this text in white.
builder->get_Font()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_DarkBlue());

builder->Writeln(u"The text color automatically chosen for this run is white.");

ASSERT_EQ(System::Drawing::Color::get_White().ToArgb(),
          doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_Runs()->idx_get(0)->get_Font()->get_AutoColor().ToArgb());

// If we change the background to a light color, black will be a more
// suitable text color than white so that the auto color will display it in black.
builder->get_Font()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightBlue());

builder->Writeln(u"The text color automatically chosen for this run is black.");

ASSERT_EQ(System::Drawing::Color::get_Black().ToArgb(),
          doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1)->get_Runs()->idx_get(0)->get_Font()->get_AutoColor().ToArgb());

doc->Save(ArtifactsDir + u"Font.SetFontAutoColor.docx");
```

## See Also

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
