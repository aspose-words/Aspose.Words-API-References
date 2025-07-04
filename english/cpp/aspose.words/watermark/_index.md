---
title: Aspose::Words::Watermark class
linktitle: Watermark
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Watermark class. Represents class to work with document watermark. To learn more, visit the  documentation article in C++.'
type: docs
weight: 76000
url: /cpp/aspose.words/watermark/
---
## Watermark class


Represents class to work with document watermark. To learn more, visit the [Working with Watermark](https://docs.aspose.com/words/cpp/working-with-watermark/) documentation article.

```cpp
class Watermark : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_Type](./get_type/)() | Gets the watermark type. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() | Removes the watermark. |
| [SetImage](./setimage/)(const System::SharedPtr\<System::Drawing::Image\>\&) | Adds Image watermark into the document. |
| [SetImage](./setimage/)(const System::SharedPtr\<System::Drawing::Image\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | Adds Image watermark into the document. |
| [SetImage](./setimage/)(const System::String\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | Adds Image watermark into the document. |
| [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | Adds Image watermark into the document. |
| [SetText](./settext/)(const System::String\&) | Adds Text watermark into the document. |
| [SetText](./settext/)(const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) | Adds Text watermark into the document. |
| static [Type](./type/)() |  |

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
