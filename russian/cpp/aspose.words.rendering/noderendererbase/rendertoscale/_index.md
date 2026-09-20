---
title: "Метод Aspose::Words::Rendering::NodeRendererBase::RenderToScale"
linktitle: "RenderToScale"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Rendering::NodeRendererBase::RenderToScale. Рисует форму в объект Graphics с указанным масштабом в C++."
type: docs
weight: 11000
url: /ru/cpp/aspose.words.rendering/noderendererbase/rendertoscale/
---
## NodeRendererBase::RenderToScale method


Отрисовывает фигуру в объект **Graphics** с указанным масштабом.

```cpp
System::Drawing::SizeF Aspose::Words::Rendering::NodeRendererBase::RenderToScale(const System::SharedPtr<System::Drawing::Graphics> &graphics, float x, float y, float scale)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| graphics | const System::SharedPtr\<System::Drawing::Graphics\>\& | Объект, в который производится отрисовка. |
| x | float | Координата X (в мировых единицах) верхнего левого угла отрисованной формы. |
| y | float | Координата Y (в мировых единицах) верхнего левого угла отрисованной формы. |
| scale | float | Масштаб для отрисовки формы (1.0 соответствует 100%). |

### ReturnValue

Ширина и высота (в мировых единицах) отрисованной формы.

## См. также

* Class [NodeRendererBase](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
