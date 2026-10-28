---
title: Aspose::Words::TextWatermarkOptions class
linktitle: TextWatermarkOptions
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::TextWatermarkOptions class. Contains options that can be specified when adding a watermark with text. To learn more, visit the Working with Watermark documentation article in C++.'
type: docs
weight: 72000
url: /cpp/aspose.words/textwatermarkoptions/
---
## TextWatermarkOptions class


Contains options that can be specified when adding a watermark with text. 
To learn more, visit the [Working with Watermark](https://docs.aspose.com/words/cpp/working-with-watermark/) documentation article.

```cpp
class TextWatermarkOptions : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo \&) const override |  |
| [TextWatermarkOptions](./textwatermarkoptions/)() |  |
| static [Type](./type/)() |  |
| [get_Color](./get_color/)() const | Gets or sets font color. The default value is **Silver**. |
| [get_FontFamily](./get_fontfamily/)() const | Gets or sets font family name. The default value is "Calibri". |
| [get_FontSize](./get_fontsize/)() const | Gets or sets a font size. The default value is 0 - auto. |
| [get_IsSemitrasparent](./get_issemitrasparent/)() const | Gets or sets a boolean value which is responsible for opacity of the watermark. The default value is **true**. |
| [get_Layout](./get_layout/)() const | Gets or sets layout of the watermark. The default value is [Diagonal](../watermarklayout/). |
| [set_Color](./set_color/)(System::Drawing::Color) | Sets font color. The default value is **Silver**. |
| [set_FontFamily](./set_fontfamily/)(const System::String \&) | Sets font family name. The default value is "Calibri". |
| [set_FontSize](./set_fontsize/)(float) | Sets a font size. The default value is 0 - auto. |
| [set_IsSemitrasparent](./set_issemitrasparent/)(bool) | Sets a boolean value which is responsible for opacity of the watermark. The default value is **true**. |
| [set_Layout](./set_layout/)(Aspose::Words::WatermarkLayout) | Sets layout of the watermark. The default value is [Diagonal](../watermarklayout/). |
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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
