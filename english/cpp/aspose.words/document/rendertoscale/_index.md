---
title: Aspose::Words::Document::RenderToScale method
linktitle: RenderToScale
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Document::RenderToScale method. Renders a document page into a Graphics object to a specified scale in C++.'
type: docs
weight: 70000
url: /cpp/aspose.words/document/rendertoscale/
---
## Document::RenderToScale method


Renders a document page into a **Graphics** object to a specified scale.

```cpp
System::Drawing::SizeF Aspose::Words::Document::RenderToScale(int32_t pageIndex, const System::SharedPtr<System::Drawing::Graphics> &graphics, float x, float y, float scale)
```


| Parameter | Type | Description |
| --- | --- | --- |
| pageIndex | int32_t | The 0-based page index. |
| graphics | const System::SharedPtr\<System::Drawing::Graphics\>\& | The object where to render to. |
| x | float | The X coordinate (in world units) of the top left corner of the rendered page. |
| y | float | The Y coordinate (in world units) of the top left corner of the rendered page. |
| scale | float | The scale for rendering the page (1.0 is 100%). |

### ReturnValue

The width and height (in world units) of the rendered page.

## Examples



Shows how to the individual pages of a document to graphics to create one image with thumbnails of all pages. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Rendering.docx");

// Calculate the number of rows and columns that we will fill with thumbnails.
const int thumbColumns = 2;
int remainder;
int thumbRows = System::Math::DivRem(doc->get_PageCount(), thumbColumns, remainder);

if (remainder > 0)
{
    thumbRows++;
}

// Scale the thumbnails relative to the size of the first page.
const float scale = 0.25f;
System::Drawing::Size thumbSize = doc->GetPageInfo(0)->GetSizeInPixels(scale, 96.0f);

// Calculate the size of the image that will contain all the thumbnails.
int imgWidth = thumbSize.get_Width() * thumbColumns;
int imgHeight = thumbSize.get_Height() * thumbRows;

{
    auto img = MakeObject<System::Drawing::Bitmap>(imgWidth, imgHeight);
    {
        SharedPtr<System::Drawing::Graphics> gr = System::Drawing::Graphics::FromImage(img);
        gr->set_TextRenderingHint(System::Drawing::Text::TextRenderingHint::AntiAliasGridFit);

        // Fill the background, which is transparent by default, in white.
        gr->FillRectangle(MakeObject<System::Drawing::SolidBrush>(System::Drawing::Color::get_White()), 0, 0, imgWidth, imgHeight);

        for (int pageIndex = 0; pageIndex < doc->get_PageCount(); pageIndex++)
        {
            int columnIdx;
            int rowIdx = System::Math::DivRem(pageIndex, thumbColumns, columnIdx);

            // Specify where we want the thumbnail to appear.
            float thumbLeft = static_cast<float>(columnIdx * thumbSize.get_Width());
            float thumbTop = static_cast<float>(rowIdx * thumbSize.get_Height());

            // Render a page as a thumbnail, and then frame it in a rectangle of the same size.
            System::Drawing::SizeF size = doc->RenderToScale(pageIndex, gr, thumbLeft, thumbTop, scale);
            gr->DrawRectangle(System::Drawing::Pens::get_Black(), thumbLeft, thumbTop, size.get_Width(), size.get_Height());
        }

        img->Save(ArtifactsDir + u"Rendering.Thumbnails.png");
    }
}
```

## See Also

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
