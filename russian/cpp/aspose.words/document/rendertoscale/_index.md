---
title: "Метод Aspose::Words::Document::RenderToScale"
linktitle: "RenderToScale"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Document::RenderToScale. Отрисовывает страницу документа в объект Graphics с указанным масштабом в C++."
type: docs
weight: 70000
url: /ru/cpp/aspose.words/document/rendertoscale/
---
## Document::RenderToScale method


Отрисовывает страницу документа в объект **Graphics** с указанным масштабом.

```cpp
System::Drawing::SizeF Aspose::Words::Document::RenderToScale(int32_t pageIndex, const System::SharedPtr<System::Drawing::Graphics> &graphics, float x, float y, float scale)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| pageIndex | int32_t | Нумерация страниц начинается с 0. |
| graphics | const System::SharedPtr\<System::Drawing::Graphics\>\& | Объект, в который производится отрисовка. |
| x | float | Координата X (в мировых единицах) верхнего левого угла отрисованной страницы. |
| y | float | Координата Y (в мировых единицах) верхнего левого угла отрисованной страницы. |
| scale | float | Масштаб для отрисовки страницы (1.0 соответствует 100%). |

### ReturnValue

Ширина и высота (в мировых единицах) отрисованной страницы.

## См. также

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
