---
title: "Aspose::Words::Rendering::ShapeRenderer class"
linktitle: "ShapeRenderer"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Rendering::ShapeRenderer class. Предоставляет методы для отрисовки отдельного Shape или GroupShape в растровое или векторное изображение или в объект Graphics. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.rendering/shaperenderer/
---
## ShapeRenderer class


Предоставляет методы для отрисовки отдельного [Shape](../../aspose.words.drawing/shape/) или [GroupShape](../../aspose.words.drawing/groupshape/) в растровое или векторное изображение или в объект Graphics. Чтобы узнать больше, посетите статью документации [Working with Shapes](https://docs.aspose.com/words/cpp/working-with-shapes/).

```cpp
class ShapeRenderer : public Aspose::Words::Rendering::NodeRendererBase
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_BoundsInPoints](../noderendererbase/get_boundsinpoints/)() const | Возвращает фактические границы фигуры в пунктах. |
| [get_OpaqueBoundsInPoints](../noderendererbase/get_opaqueboundsinpoints/)() | Возвращает непрозрачные границы фигуры в пунктах. |
| [get_SizeInPoints](../noderendererbase/get_sizeinpoints/)() | Возвращает фактический размер фигуры в пунктах. |
| [GetBoundsInPixels](../noderendererbase/getboundsinpixels/)(float, float) | Вычисляет границы фигуры в пикселях для указанного коэффициента масштабирования и разрешения. |
| [GetBoundsInPixels](../noderendererbase/getboundsinpixels/)(float, float, float) | Вычисляет границы фигуры в пикселях для указанного коэффициента масштабирования и разрешения. |
| [GetOpaqueBoundsInPixels](../noderendererbase/getopaqueboundsinpixels/)(float, float) | Вычисляет непрозрачные границы фигуры в пикселях для указанного коэффициента масштабирования и разрешения. |
| [GetOpaqueBoundsInPixels](../noderendererbase/getopaqueboundsinpixels/)(float, float, float) | Вычисляет непрозрачные границы фигуры в пикселях для указанного коэффициента масштабирования и разрешения. |
| [GetSizeInPixels](../noderendererbase/getsizeinpixels/)(float, float) | Вычисляет размер фигуры в пикселях для указанного коэффициента масштабирования и разрешения. |
| [GetSizeInPixels](../noderendererbase/getsizeinpixels/)(float, float, float) | Вычисляет размер фигуры в пикселях для указанного коэффициента масштабирования и разрешения. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [NodeRendererBase](../noderendererbase/noderendererbase/)() |  |
| [RenderToScale](../noderendererbase/rendertoscale/)(const System::SharedPtr\<System::Drawing::Graphics\>\&, float, float, float) | Отрисовывает фигуру в объект **Graphics** с указанным масштабом. |
| [RenderToSize](../noderendererbase/rendertosize/)(const System::SharedPtr\<System::Drawing::Graphics\>\&, float, float, float, float) | Отрисовывает фигуру в объект **Graphics** с указанным размером. |
| [Save](../noderendererbase/save/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) | Отрисовывает фигуру в изображение и сохраняет в файл. |
| [Save](../noderendererbase/save/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) | Отрисовывает фигуру в SVG‑изображение и сохраняет в файл. |
| [Save](../noderendererbase/save/)(const System::SharedPtr\<System::IO::Stream\>\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) | Отрисовывает фигуру в изображение и сохраняет в поток. |
| [Save](../noderendererbase/save/)(const System::SharedPtr\<System::IO::Stream\>\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) | Отрисовывает фигуру в SVG‑изображение и сохраняет в поток. |
| [Save](../noderendererbase/save/)(std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) |  |
| [Save](../noderendererbase/save/)(std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) |  |
| [ShapeRenderer](./shaperenderer/)(const System::SharedPtr\<Aspose::Words::Drawing::ShapeBase\>\&) | Инициализирует новый экземпляр этого класса. |
| static [Type](./type/)() |  |
## См. также

* Class [NodeRendererBase](../noderendererbase/)
* Namespace [Aspose::Words::Rendering](../)
* Library [Aspose.Words for C++](../../)
