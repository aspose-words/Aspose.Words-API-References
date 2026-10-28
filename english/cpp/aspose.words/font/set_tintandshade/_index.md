---
title: Aspose::Words::Font::set_TintAndShade method
linktitle: set_TintAndShade
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Font::set_TintAndShade method. Sets a double value that lightens or darkens a color in C++.'
type: docs
weight: 106000
url: /cpp/aspose.words/font/set_tintandshade/
---
## Font::set_TintAndShade method


Sets a double value that lightens or darkens a color.

```cpp
void Aspose::Words::Font::set_TintAndShade(double value)
```

## Remarks


 The allowed values are in range from -1 (darkest) to 1 (lightest) for this property.

Zero (0) is neutral.
## Examples


Shows how to create and use themed style.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln();

// Create some style with theme font properties.
System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->Add(StyleType::Paragraph, u"ThemedStyle");
style->get_Font()->set_ThemeFont(ThemeFont::Major);
style->get_Font()->set_ThemeColor(ThemeColor::Accent5);
style->get_Font()->set_TintAndShade(0.3);

builder->get_ParagraphFormat()->set_StyleName(u"ThemedStyle");
builder->Writeln(u"Text with themed style");
```
## Exceptions

* **ArgumentOutOfRangeException** - Throw if set this property to a value less than -1 or more than 1.
* **InvalidOperationException** - Throw if set this property for [Font](../) object with non-theme colors.

## See Also

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
