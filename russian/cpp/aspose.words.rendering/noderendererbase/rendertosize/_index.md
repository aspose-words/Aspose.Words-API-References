---
title: "Aspose::Words::Rendering::NodeRendererBase::RenderToSize метод"
linktitle: "RenderToSize"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Rendering::NodeRendererBase::RenderToSize method. Отрисовывает фигуру в объект Graphics до указанного размера в C++."
type: docs
weight: 12000
url: /ru/cpp/aspose.words.rendering/noderendererbase/rendertosize/
---
## NodeRendererBase::RenderToSize method


Отрисовывает фигуру в объект **Graphics** с указанным размером.

```cpp
float Aspose::Words::Rendering::NodeRendererBase::RenderToSize(const System::SharedPtr<System::Drawing::Graphics> &graphics, float x, float y, float width, float height)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| graphics | const System::SharedPtr\<System::Drawing::Graphics\>\& | Объект, в который производится отрисовка. |
| x | float | Координата X (в мировых единицах) верхнего левого угла отрисованной формы. |
| y | float | Координата Y (в мировых единицах) верхнего левого угла отрисованной формы. |
| width | float | Максимальная ширина (в мировых единицах), которую может занимать отрисованная фигура. |
| height | float | Максимальная высота (в мировых единицах), которую может занимать отрисованная фигура. |

### ReturnValue

Масштаб, который был автоматически рассчитан для отрисованной фигуры, чтобы соответствовать указанному размеру.

## См. также

* Class [NodeRendererBase](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
