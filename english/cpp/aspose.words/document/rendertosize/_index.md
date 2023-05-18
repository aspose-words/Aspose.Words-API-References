---
title: Aspose::Words::Document::RenderToSize method
linktitle: RenderToSize
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Document::RenderToSize method. Renders a document page into a object to a specified size in C++.'
type: docs
weight: 71000
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

## See Also

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
