---
title: "Aspose::Words::Document::RenderToSize метод"
linktitle: "RenderToSize"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Document::RenderToSize метод. Рендерит страницу документа в объект Graphics до указанного размера в C++."
type: docs
weight: 71000
url: /ru/cpp/aspose.words/document/rendertosize/
---
## Document::RenderToSize method


Отрисовывает страницу документа в объект **Graphics** с указанным размером.

```cpp
float Aspose::Words::Document::RenderToSize(int32_t pageIndex, const System::SharedPtr<System::Drawing::Graphics> &graphics, float x, float y, float width, float height)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| pageIndex | int32_t | Нумерация страниц начинается с 0. |
| graphics | const System::SharedPtr\<System::Drawing::Graphics\>\& | Объект, в который производится отрисовка. |
| x | float | Координата X (в мировых единицах) верхнего левого угла отрисованной страницы. |
| y | float | Координата Y (в мировых единицах) верхнего левого угла отрисованной страницы. |
| width | float | Максимальная ширина (в мировых единицах), которую может занимать отрисованная страница. |
| height | float | Максимальная высота (в мировых единицах), которую может занимать отрисованная страница. |

### ReturnValue

Масштаб, который был автоматически рассчитан для отрисованной страницы, чтобы она соответствовала указанному размеру.

## См. также

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
