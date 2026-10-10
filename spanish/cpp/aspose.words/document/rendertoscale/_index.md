---
title: "Aspose::Words::Document::RenderToScale método"
linktitle: "RenderToScale"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Document::RenderToScale método. Renderiza una página del documento en un objeto Graphics a una escala especificada en C++."
type: docs
weight: 70000
url: /es/cpp/aspose.words/document/rendertoscale/
---
## Document::RenderToScale method


Renderiza una página del documento en un objeto **Graphics** a una escala especificada.

```cpp
System::Drawing::SizeF Aspose::Words::Document::RenderToScale(int32_t pageIndex, const System::SharedPtr<System::Drawing::Graphics> &graphics, float x, float y, float scale)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| pageIndex | int32_t | El índice de página basado en cero. |
| graphics | const System::SharedPtr\<System::Drawing::Graphics\>\& | El objeto donde renderizar. |
| x | float | La coordenada X (en unidades del mundo) de la esquina superior izquierda de la página renderizada. |
| y | float | La coordenada Y (en unidades del mundo) de la esquina superior izquierda de la página renderizada. |
| scale | float | La escala para renderizar la página (1.0 es 100%). |

### ReturnValue

El ancho y la altura (en unidades del mundo) de la página renderizada.

## Ver también

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
