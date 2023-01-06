---
title: WatermarkType
second_title: Aspose.Words for C++ API Reference
description: Specifies the watermark type.
type: docs
weight: 1704
url: /cpp/aspose.words/watermarktype/
---
## WatermarkType enum


Specifies the watermark type.

```cpp
enum class WatermarkType
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Text | 0 | Indicates that the text will be used as a watermark. Such a watermark corresponds to a WordArt object. |
| Image | 1 | Indicates that the image will be used as a watermark. Such a watermark corresponds to a shape with image. |
| None | 2 | Indicates watermark is no set. |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words](../../)
