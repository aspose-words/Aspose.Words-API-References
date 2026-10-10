---
title: "Aspose::Words::Rendering::ShapeRenderer class"
linktitle: "ShapeRenderer"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Rendering::ShapeRenderer class. يوفر طرقًا لتصوير شكل فردي أو GroupShape إلى صورة نقطية أو متجهة أو إلى كائن Graphics. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words.rendering/shaperenderer/
---
## ShapeRenderer class


يوفر طرقًا لتصوير [Shape](../../aspose.words.drawing/shape/) أو [GroupShape](../../aspose.words.drawing/groupshape/) فرديًا إلى صورة نقطية أو متجهة أو إلى كائن Graphics. لمعرفة المزيد، زر مقالة الوثائق [Working with Shapes](https://docs.aspose.com/words/cpp/working-with-shapes/).

```cpp
class ShapeRenderer : public Aspose::Words::Rendering::NodeRendererBase
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_BoundsInPoints](../noderendererbase/get_boundsinpoints/)() const | يحصل على الحدود الفعلية للشكل بالنقاط. |
| [get_OpaqueBoundsInPoints](../noderendererbase/get_opaqueboundsinpoints/)() | يحصل على الحدود غير الشفافة للشكل بالنقاط. |
| [get_SizeInPoints](../noderendererbase/get_sizeinpoints/)() | يحصل على الحجم الفعلي للشكل بالنقاط. |
| [GetBoundsInPixels](../noderendererbase/getboundsinpixels/)(float, float) | يحسب حدود الشكل بالبكسل لعامل تكبير ودقة محددين. |
| [GetBoundsInPixels](../noderendererbase/getboundsinpixels/)(float, float, float) | يحسب حدود الشكل بالبكسل لعامل تكبير ودقة محددين. |
| [GetOpaqueBoundsInPixels](../noderendererbase/getopaqueboundsinpixels/)(float, float) | يحسب الحدود غير الشفافة للشكل بالبكسل لعامل تكبير ودقة محددين. |
| [GetOpaqueBoundsInPixels](../noderendererbase/getopaqueboundsinpixels/)(float, float, float) | يحسب الحدود غير الشفافة للشكل بالبكسل لعامل تكبير ودقة محددين. |
| [GetSizeInPixels](../noderendererbase/getsizeinpixels/)(float, float) | يحسب حجم الشكل بالبكسل لعامل تكبير ودقة محددين. |
| [GetSizeInPixels](../noderendererbase/getsizeinpixels/)(float, float, float) | يحسب حجم الشكل بالبكسل لعامل تكبير ودقة محددين. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [NodeRendererBase](../noderendererbase/noderendererbase/)() |  |
| [RenderToScale](../noderendererbase/rendertoscale/)(const System::SharedPtr\<System::Drawing::Graphics\>\&, float, float, float) | يرسم الشكل داخل كائن **Graphics** إلى مقياس محدد. |
| [RenderToSize](../noderendererbase/rendertosize/)(const System::SharedPtr\<System::Drawing::Graphics\>\&, float, float, float, float) | يرسم الشكل داخل كائن **Graphics** إلى حجم محدد. |
| [Save](../noderendererbase/save/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) | يرسم الشكل إلى صورة ويحفظها في ملف. |
| [Save](../noderendererbase/save/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) | يرسم الشكل إلى صورة SVG ويحفظها في ملف. |
| [Save](../noderendererbase/save/)(const System::SharedPtr\<System::IO::Stream\>\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) | يرسم الشكل إلى صورة ويحفظها في تدفق. |
| [Save](../noderendererbase/save/)(const System::SharedPtr\<System::IO::Stream\>\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) | يرسم الشكل إلى صورة SVG ويحفظها في تدفق. |
| [Save](../noderendererbase/save/)(std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) |  |
| [Save](../noderendererbase/save/)(std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) |  |
| [ShapeRenderer](./shaperenderer/)(const System::SharedPtr\<Aspose::Words::Drawing::ShapeBase\>\&) | يُنشئ مثيلًا جديدًا لهذه الفئة. |
| static [Type](./type/)() |  |
## انظر أيضًا

* Class [NodeRendererBase](../noderendererbase/)
* Namespace [Aspose::Words::Rendering](../)
* Library [Aspose.Words for C++](../../)
