---
title: "طريقة Aspose::Words::Document::RenderToScale"
linktitle: "RenderToScale"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Document::RenderToScale. تُعيد رسم صفحة المستند داخل كائن Graphics إلى مقياس محدد في C++."
type: docs
weight: 70000
url: /ar/cpp/aspose.words/document/rendertoscale/
---
## Document::RenderToScale method


يرسم صفحة المستند في كائن **Graphics** إلى مقياس محدد.

```cpp
System::Drawing::SizeF Aspose::Words::Document::RenderToScale(int32_t pageIndex, const System::SharedPtr<System::Drawing::Graphics> &graphics, float x, float y, float scale)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| pageIndex | int32_t | مؤشر الصفحة بدءًا من الصفر. |
| graphics | const System::SharedPtr\<System::Drawing::Graphics\>\& | الكائن الذي يتم الرسم إليه. |
| x | float | الإحداثي X (بوحدات العالم) للزاوية العلوية اليسرى للصفحة المُرَسَمة. |
| y | float | الإحداثي Y (بوحدات العالم) للزاوية العلوية اليسرى للصفحة المُرَسَمة. |
| scale | float | المقياس المستخدم في رسم الصفحة (1.0 يساوي 100%). |

### ReturnValue

العرض والارتفاع (بوحدات العالم) للصفحة المُرَسَمة.

## انظر أيضًا

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
