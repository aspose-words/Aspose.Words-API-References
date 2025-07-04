---
title: Aspose::Words::WatermarkLayout enum
linktitle: WatermarkLayout
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::WatermarkLayout enum. Defines layout of the watermark relative to the watermark center in C++.'
type: docs
weight: 130000
url: /cpp/aspose.words/watermarklayout/
---
## WatermarkLayout enum


Defines layout of the watermark relative to the watermark center.

```cpp
enum class WatermarkLayout
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Horizontal | 0 | Horizontal watermark layout. Corresponds to 0 degrees of rotation. |
| Diagonal | 315 | Diagonal watermark layout. Corresponds to 315 degrees of rotation. |


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
textWatermarkOptions->set_FontSize(36.0f);
textWatermarkOptions->set_Color(System::Drawing::Color::get_Black());
textWatermarkOptions->set_Layout(Aspose::Words::WatermarkLayout::Diagonal);
textWatermarkOptions->set_IsSemitrasparent(false);

doc->get_Watermark()->SetText(u"Aspose Watermark", textWatermarkOptions);

doc->Save(get_ArtifactsDir() + u"Document.TextWatermark.docx");

// We can remove a watermark from a document like this.
if (doc->get_Watermark()->get_Type() == Aspose::Words::WatermarkType::Text)
{
    doc->get_Watermark()->Remove();
}
```

## See Also

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
