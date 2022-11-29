---
title: RenderToSize
second_title: Aspose.Words for C++ API Reference
description: Renders a document page into a object to a specified size.
type: docs
weight: 846
url: /cpp/aspose.words/document/rendertosize/
---
## Document::RenderToSize method


Renders a document page into a object to a specified size.

```cpp
float Aspose::Words::Document::RenderToSize(int32_t pageIndex, const System::SharedPtr<System::Drawing::Graphics> &graphics, float x, float y, float width, float height)
```


| Parameter | Type | Description |
| --- | --- | --- |
| pageIndex | int32_t | The 0-based page index. |
| graphics | const System::SharedPtr\<System::Drawing::Graphics\>\& | The object where to render to. |
| x | float | The X coordinate (in world units) of the top left corner of the rendered page. |
| y | float | The Y coordinate (in world units) of the top left corner of the rendered page. |
| width | float | The maximum width (in world units) that can be occupied by the rendered page. |
| height | float | The maximum height (in world units) that can be occupied by the rendered page. |

### ReturnValue

The scale that was automatically calculated for the rendered page to fit the specified size.

## Examples



Shows how to render a document to a bitmap at a specified location and size. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Rendering.docx");

{
    auto bmp = MakeObject<System::Drawing::Bitmap>(700, 700);
    {
        SharedPtr<System::Drawing::Graphics> gr = System::Drawing::Graphics::FromImage(bmp);
        gr->set_TextRenderingHint(System::Drawing::Text::TextRenderingHint::AntiAliasGridFit);

        // Set the "PageUnit" property to "GraphicsUnit.Inch" to use inches as the
        // measurement unit for any transformations and dimensions that we will define.
        gr->set_PageUnit(System::Drawing::GraphicsUnit::Inch);

        // Offset the output 0.5" from the edge.
        gr->TranslateTransform(0.5f, 0.5f);

        // Rotate the output by 10 degrees.
        gr->RotateTransform(10.0f);

        // Draw a 3"x3" rectangle.
        gr->DrawRectangle(MakeObject<System::Drawing::Pen>(System::Drawing::Color::get_Black(), 3.f / 72.f), 0.f, 0.f, 3.f, 3.f);

        // Draw the first page of our document with the same dimensions and transformation as the rectangle.
        // The rectangle will frame the first page.
        float returnedScale = doc->RenderToSize(0, gr, 0.f, 0.f, 3.f, 3.f);

        // This is the scaling factor that the RenderToSize method applied to the first page to fit the specified size.
        ASSERT_NEAR(0.2566f, returnedScale, 0.0001f);

        // Set the "PageUnit" property to "GraphicsUnit.Millimeter" to use millimeters as the
        // measurement unit for any transformations and dimensions that we will define.
        gr->set_PageUnit(System::Drawing::GraphicsUnit::Millimeter);

        // Reset the transformations that we used from the previous rendering.
        gr->ResetTransform();

        // Apply another set of transformations.
        gr->TranslateTransform(10.0f, 10.0f);
        gr->ScaleTransform(0.5f, 0.5f);
        gr->set_PageScale(2.f);

        // Create another rectangle and use it to frame another page from the document.
        gr->DrawRectangle(MakeObject<System::Drawing::Pen>(System::Drawing::Color::get_Black(), 1.0f), 90, 10, 50, 100);
        doc->RenderToSize(1, gr, 90.0f, 10.0f, 50.0f, 100.0f);

        bmp->Save(ArtifactsDir + u"Rendering.RenderToSize.png");
    }
}
```

## See Also

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
