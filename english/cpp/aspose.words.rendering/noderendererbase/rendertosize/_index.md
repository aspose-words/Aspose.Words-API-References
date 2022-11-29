---
title: RenderToSize
second_title: Aspose.Words for C++ API Reference
description: Renders the shape into a Graphics object to a specified size.
type: docs
weight: 105
url: /cpp/aspose.words.rendering/noderendererbase/rendertosize/
---
## NodeRendererBase::RenderToSize method


Renders the shape into a **Graphics** object to a specified size.

```cpp
float Aspose::Words::Rendering::NodeRendererBase::RenderToSize(const System::SharedPtr<System::Drawing::Graphics> &graphics, float x, float y, float width, float height)
```


| Parameter | Type | Description |
| --- | --- | --- |
| graphics | const System::SharedPtr\<System::Drawing::Graphics\>\& | The object where to render to. |
| x | float | The X coordinate (in world units) of the top left corner of the rendered shape. |
| y | float | The Y coordinate (in world units) of the top left corner of the rendered shape. |
| width | float | The maximum width (in world units) that can be occupied by the rendered shape. |
| height | float | The maximum height (in world units) that can be occupied by the rendered shape. |

### ReturnValue

The scale that was automatically calculated for the rendered shape to fit the specified size.

## See Also

* Class [NodeRendererBase](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words](../../../)
