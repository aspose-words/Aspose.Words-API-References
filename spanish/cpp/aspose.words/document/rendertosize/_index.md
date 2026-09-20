---
title: "Método Aspose::Words::Document::RenderToSize"
linktitle: "RenderToSize"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Document::RenderToSize. Renderiza una página del documento en un objeto Graphics con un tamaño especificado en C++."
type: docs
weight: 71000
url: /es/cpp/aspose.words/document/rendertosize/
---
## Document::RenderToSize method


Renderiza una página del documento en un objeto **Graphics** a un tamaño especificado.

```cpp
float Aspose::Words::Document::RenderToSize(int32_t pageIndex, const System::SharedPtr<System::Drawing::Graphics> &graphics, float x, float y, float width, float height)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| pageIndex | int32_t | El índice de página basado en cero. |
| graphics | const System::SharedPtr\<System::Drawing::Graphics\>\& | El objeto donde renderizar. |
| x | float | La coordenada X (en unidades del mundo) de la esquina superior izquierda de la página renderizada. |
| y | float | La coordenada Y (en unidades del mundo) de la esquina superior izquierda de la página renderizada. |
| ancho | float | El ancho máximo (en unidades del mundo) que puede ocupar la página renderizada. |
| alto | float | La altura máxima (en unidades del mundo) que puede ocupar la página renderizada. |

### ReturnValue

La escala que se calculó automáticamente para que la página renderizada se ajuste al tamaño especificado.

## Ver también

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
