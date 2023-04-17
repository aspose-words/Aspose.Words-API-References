---
title: Aspose::Words::TextWatermarkOptions::get_FontSize method
linktitle: get_FontSize
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::TextWatermarkOptions::get_FontSize method. Gets or sets a font size. The default value is 0 - auto in C++.'
type: docs
weight: 5000
url: /cpp/aspose.words/textwatermarkoptions/get_fontsize/
---
## TextWatermarkOptions::get_FontSize method


Gets or sets a font size. The default value is 0 - auto.

```cpp
float Aspose::Words::TextWatermarkOptions::get_FontSize() const
```

## Remarks


Valid values range from 0 to 65.5 inclusive.

Auto font size means that the watermark will be scaled to its max width and max height relative to the page margins.

## Examples



Shows how to create a text watermark. 
```cpp
auto doc = MakeObject<Document>();

// Add a plain text watermark.
doc->get_Watermark()->SetText(u"Aspose Watermark");

// If we wish to edit the text formatting using it as a watermark,
// we can do so by passing a TextWatermarkOptions object when creating the watermark.
auto textWatermarkOptions = MakeObject<TextWatermarkOptions>();
textWatermarkOptions->set_FontFamily(u"Arial");
textWatermarkOptions->set_FontSize(36.0f);
textWatermarkOptions->set_Color(System::Drawing::Color::get_Black());
textWatermarkOptions->set_Layout(WatermarkLayout::Diagonal);
textWatermarkOptions->set_IsSemitrasparent(false);

doc->get_Watermark()->SetText(u"Aspose Watermark", textWatermarkOptions);

doc->Save(ArtifactsDir + u"Document.TextWatermark.docx");

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
