---
title: "Clase Aspose::Words::Rendering::PageInfo"
linktitle: "PageInfo"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::Rendering::PageInfo. Representa información sobre una página de documento particular. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.rendering/pageinfo/
---
## PageInfo class


Representa información sobre una página de documento específica. Para obtener más información, visite el artículo de documentación [Rendering](https://docs.aspose.com/words/cpp/rendering/).

```cpp
class PageInfo : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_Colored](./get_colored/)() | Devuelve **true** si la página contiene contenido coloreado. |
| [get_HeightInPoints](./get_heightinpoints/)() | Obtiene la altura de la página en puntos. |
| [get_Landscape](./get_landscape/)() const | Devuelve **true** si la orientación de la página especificada en el documento para esta página es horizontal. |
| [get_PaperSize](./get_papersize/)() | Obtiene el tamaño del papel como enumeración. |
| [get_PaperTray](./get_papertray/)() const | Obtiene la bandeja de papel (cajón) para esta página según lo especificado en el documento. El valor es específico de la implementación (impresora). |
| [get_SizeInPoints](./get_sizeinpoints/)() const | Obtiene el tamaño de la página en puntos. |
| [get_WidthInPoints](./get_widthinpoints/)() | Obtiene el ancho de la página en puntos. |
| [GetSizeInPixels](./getsizeinpixels/)(float, float) | Calcula el tamaño de la página en píxeles para un factor de zoom y resolución especificados. |
| [GetSizeInPixels](./getsizeinpixels/)(float, float, float) | Calcula el tamaño de la página en píxeles para un factor de zoom y resolución especificados. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Observaciones


El ancho y la altura de la página devueltos por este objeto representan el tamaño \"final\" de la página, p. ej., ya están rotados a la orientación correcta.

## Ver también

* Namespace [Aspose::Words::Rendering](../)
* Library [Aspose.Words for C++](../../)
