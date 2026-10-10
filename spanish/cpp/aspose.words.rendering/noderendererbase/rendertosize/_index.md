---
title: "Método Aspose::Words::Rendering::NodeRendererBase::RenderToSize"
linktitle: "RenderToSize"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Rendering::NodeRendererBase::RenderToSize. Renderiza la forma en un objeto Graphics a un tamaño especificado en C++."
type: docs
weight: 12000
url: /es/cpp/aspose.words.rendering/noderendererbase/rendertosize/
---
## NodeRendererBase::RenderToSize method


Renderiza la forma en un objeto **Graphics** a un tamaño especificado.

```cpp
float Aspose::Words::Rendering::NodeRendererBase::RenderToSize(const System::SharedPtr<System::Drawing::Graphics> &graphics, float x, float y, float width, float height)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| graphics | const System::SharedPtr\<System::Drawing::Graphics\>\& | El objeto donde renderizar. |
| x | float | La coordenada X (en unidades del mundo) de la esquina superior izquierda de la forma renderizada. |
| y | float | La coordenada Y (en unidades del mundo) de la esquina superior izquierda de la forma renderizada. |
| ancho | float | El ancho máximo (en unidades del mundo) que puede ocupar la forma renderizada. |
| alto | float | La altura máxima (en unidades del mundo) que puede ocupar la forma renderizada. |

### ReturnValue

La escala que se calculó automáticamente para la forma renderizada para ajustarse al tamaño especificado.

## Ver también

* Class [NodeRendererBase](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
