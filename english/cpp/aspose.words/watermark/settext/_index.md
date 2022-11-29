---
title: SetText
second_title: Aspose.Words for C++ API Reference
description: Adds Text watermark into the document.
type: docs
weight: 40
url: /cpp/aspose.words/watermark/settext/
---
## Watermark::SetText(const System::String\&) method


Adds Text watermark into the document.

```cpp
void Aspose::Words::Watermark::SetText(const System::String &text)
```


| Parameter | Type | Description |
| --- | --- | --- |
| text | const System::String\& | Text that is displayed as a watermark. |

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

* Class [Watermark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
## Watermark::SetText(const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) method


Adds Text watermark into the document.

```cpp
void Aspose::Words::Watermark::SetText(const System::String &text, const System::SharedPtr<Aspose::Words::TextWatermarkOptions> &options)
```


| Parameter | Type | Description |
| --- | --- | --- |
| text | const System::String\& | Text that is displayed as a watermark. |
| options | const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\& | Defines additional options for the text watermark. |

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

* Class [TextWatermarkOptions](../../textwatermarkoptions/)
* Class [Watermark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
