---
title: Aspose::Words::Watermark::SetText method
linktitle: SetText
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Watermark::SetText method. Adds Text watermark into the document in C++.'
type: docs
weight: 7000
url: /cpp/aspose.words/watermark/settext/
---
## Watermark::SetText(const System::String \&) method


Adds Text watermark into the document.

```cpp
void Aspose::Words::Watermark::SetText(const System::String & text)
```


| Parameter | Type | Description |
| --- | --- | --- |
| text | const System::String \& | Text that is displayed as a watermark. |
## Remarks

 The text length must be in the range from 1 to 200 inclusive. The text cannot be **null** or contain only whitespaces. 
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
## Exceptions

* **ArgumentOutOfRangeException** -  Throws when the text length is out of range or the text contains only whitespaces.
* **ArgumentNullException** -  Throws when the text is **null**.

## See Also

* Class [Watermark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Watermark::SetText(const System::String \&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\> \&) method


Adds Text watermark into the document.

```cpp
void Aspose::Words::Watermark::SetText(const System::String & text, const System::SharedPtr<Aspose::Words::TextWatermarkOptions> & options)
```


| Parameter | Type | Description |
| --- | --- | --- |
| text | const System::String \& | Text that is displayed as a watermark. |
| options | const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\> \& | Defines additional options for the text watermark. |
## Remarks

 The text length must be in the range from 1 to 200 inclusive. The text cannot be **null** or contain only whitespaces. If [TextWatermarkOptions](../../textwatermarkoptions/) is **null**, the watermark will be set with default options.
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
## Exceptions

* **ArgumentOutOfRangeException** -  Throws when the text length is out of range or the text contain only whitespaces.
* **ArgumentNullException** -  Throws when the text is **null**.

## See Also

* Class [Watermark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
