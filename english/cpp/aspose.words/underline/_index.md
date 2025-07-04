---
title: Aspose::Words::Underline enum
linktitle: Underline
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Underline enum. Indicates type of the underline applied to a font in C++.'
type: docs
weight: 126000
url: /cpp/aspose.words/underline/
---
## Underline enum


Indicates type of the underline applied to a font.

```cpp
enum class Underline
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| None | 0 |  |
| Single | 1 |  |
| Words | 2 |  |
| Double | 3 |  |
| Dotted | 4 |  |
| Thick | 6 |  |
| Dash | 7 |  |
| DashLong | 39 |  |
| DotDash | 9 |  |
| DotDotDash | 10 |  |
| Wavy | 11 |  |
| DottedHeavy | 20 |  |
| DashHeavy | 23 |  |
| DashLongHeavy | 55 |  |
| DotDashHeavy | 25 |  |
| DotDotDashHeavy | 26 |  |
| WavyHeavy | 27 |  |
| WavyDouble | 43 |  |


## Examples



Shows how to insert a hyperlink field. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"For more information, please visit the ");

// Insert a hyperlink and emphasize it with custom formatting.
// The hyperlink will be a clickable piece of text which will take us to the location specified in the URL.
builder->get_Font()->set_Color(System::Drawing::Color::get_Blue());
builder->get_Font()->set_Underline(Aspose::Words::Underline::Single);
builder->InsertHyperlink(u"Google website", u"https://www.google.com", false);
builder->get_Font()->ClearFormatting();
builder->Writeln(u".");

// Ctrl + left clicking the link in the text in Microsoft Word will take us to the URL via a new web browser window.
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertHyperlink.docx");
```

## See Also

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
