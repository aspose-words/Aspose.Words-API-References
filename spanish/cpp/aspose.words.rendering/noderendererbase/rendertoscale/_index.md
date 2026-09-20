---
title: "Método Aspose::Words::Rendering::NodeRendererBase::RenderToScale"
linktitle: "RenderToScale"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Rendering::NodeRendererBase::RenderToScale. Renderiza la forma en un objeto Graphics a una escala especificada en C++."
type: docs
weight: 11000
url: /es/cpp/aspose.words.rendering/noderendererbase/rendertoscale/
---
## NodeRendererBase::RenderToScale method


Renderiza la forma en un objeto **Graphics** a una escala especificada.

```cpp
System::Drawing::SizeF Aspose::Words::Rendering::NodeRendererBase::RenderToScale(const System::SharedPtr<System::Drawing::Graphics> &graphics, float x, float y, float scale)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| graphics | const System::SharedPtr\<System::Drawing::Graphics\>\& | El objeto donde renderizar. |
| x | float | La coordenada X (en unidades del mundo) de la esquina superior izquierda de la forma renderizada. |
| y | float | La coordenada Y (en unidades del mundo) de la esquina superior izquierda de la forma renderizada. |
| scale | float | La escala para renderizar la forma (1.0 es 100%). |

### ReturnValue

El ancho y la altura (en unidades del mundo) de la forma renderizada.

## Ver también

* Class [NodeRendererBase](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
