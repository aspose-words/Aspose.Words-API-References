---
title: "طريقة Aspose::Words::Rendering::NodeRendererBase::RenderToScale"
linktitle: "RenderToScale"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Rendering::NodeRendererBase::RenderToScale. تقوم برسم الشكل داخل كائن Graphics إلى مقياس محدد في C++."
type: docs
weight: 11000
url: /ar/cpp/aspose.words.rendering/noderendererbase/rendertoscale/
---
## NodeRendererBase::RenderToScale method


يرسم الشكل داخل كائن **Graphics** إلى مقياس محدد.

```cpp
System::Drawing::SizeF Aspose::Words::Rendering::NodeRendererBase::RenderToScale(const System::SharedPtr<System::Drawing::Graphics> &graphics, float x, float y, float scale)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| graphics | const System::SharedPtr\<System::Drawing::Graphics\>\& | الكائن الذي يتم الرسم إليه. |
| x | float | إحداثي X (بوحدات العالم) للزاوية العلوية اليسرى للشكل المُرسم. |
| y | float | إحداثي Y (بوحدات العالم) للزاوية العلوية اليسرى للشكل المُرسم. |
| scale | float | مقياس عرض الشكل (1.0 يساوي 100%). |

### ReturnValue

العرض والارتفاع (بوحدات العالم) للشكل المُرسم.

## انظر أيضًا

* Class [NodeRendererBase](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
