---
title: Aspose::Words::TextWatermarkOptions::set_FontFamily method
linktitle: set_FontFamily
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::TextWatermarkOptions::set_FontFamily method. Sets font family name. The default value is "Calibri" in C++.'
type: docs
weight: 11000
url: /cpp/aspose.words/textwatermarkoptions/set_fontfamily/
---
## TextWatermarkOptions::set_FontFamily method


Sets font family name. The default value is "Calibri".

```cpp
void Aspose::Words::TextWatermarkOptions::set_FontFamily(const System::String & value)
```

## Examples


Shows how to create a text watermark.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Add a plain text watermark.
doc->get_Watermark()->SetText(u"Aspose Watermark");

// If we wish to edit the text formatting using it as a watermark,
// we can do so by passing a TextWatermarkOptions object when creating the watermark.
auto textWatermarkOptions = System::MakeObject<Aspose::Words::TextWatermarkOptions>();
textWatermarkOptions->set_FontFamily(u"Arial");
textWatermarkOptions->set_FontSize(36);
textWatermarkOptions->set_Color(System::Drawing::Color::get_Black());
textWatermarkOptions->set_Layout(WatermarkLayout::Diagonal);
textWatermarkOptions->set_IsSemitrasparent(false);

doc->get_Watermark()->SetText(u"Aspose Watermark", textWatermarkOptions);

doc->Save(get_ArtifactsDir() + u"Document.TextWatermark.docx");

// We can remove a watermark from a document like this.
if (doc->get_Watermark()->get_Type() == WatermarkType::Text)
{
    doc->get_Watermark()->Remove();
}
```
## See Also

* Class [TextWatermarkOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
