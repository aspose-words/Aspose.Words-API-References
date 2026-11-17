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

## See Also

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
