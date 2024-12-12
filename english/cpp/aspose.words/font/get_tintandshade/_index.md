---
title: Aspose::Words::Font::get_TintAndShade method
linktitle: get_TintAndShade
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Font::get_TintAndShade method. Gets or sets a double value that lightens or darkens a color in C++.'
type: docs
weight: 54000
url: /cpp/aspose.words/font/get_tintandshade/
---
## Font::get_TintAndShade method


Gets or sets a double value that lightens or darkens a color.

```cpp
double Aspose::Words::Font::get_TintAndShade()
```

## Remarks


The allowed values are in range from -1 (darkest) to 1 (lightest) for this property.

Zero (0) is neutral.

## Examples



Shows how to create and use themed style. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->Writeln();

// Create some style with theme font properties.
SharedPtr<Style> style = doc->get_Styles()->Add(StyleType::Paragraph, u"ThemedStyle");
style->get_Font()->set_ThemeFont(ThemeFont::Major);
style->get_Font()->set_ThemeColor(ThemeColor::Accent5);
style->get_Font()->set_TintAndShade(0.3);

builder->get_ParagraphFormat()->set_StyleName(u"ThemedStyle");
builder->Writeln(u"Text with themed style");
```

## See Also

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
