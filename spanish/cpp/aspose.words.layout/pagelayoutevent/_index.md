---
title: "Aspose::Words::Layout::PageLayoutEvent enum"
linktitle: "PageLayoutEvent"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Layout::PageLayoutEvent enum. Un código de evento generado durante la construcción y renderizado del modelo de diseño de página. El modelo de diseño de página se construye en dos pasos. Primero, \"paso de conversión\", que es cuando el diseño de página extrae el contenido del documento y crea el grafo de objetos. Segundo, \"paso de reflujo\", que es cuando las estructuras se dividen, se fusionan y se organizan en páginas. Dependiendo de la operación que desencadenó la construcción, el modelo de diseño de página puede o no renderizarse posteriormente en un formato de página fija. Por ejemplo, calcular el número de páginas del documento o actualizar campos no requiere renderizado, mientras que la exportación a PDF sí lo hace en C++."
type: docs
weight: 10000
url: /es/cpp/aspose.words.layout/pagelayoutevent/
---
## PageLayoutEvent enum


Código del evento generado durante la construcción y renderizado del modelo de diseño de página. El modelo de diseño de página se construye en dos pasos. Primero, "paso de conversión", que es cuando el diseño de página extrae el contenido del documento y crea el grafo de objetos. Segundo, "paso de reflujo", que es cuando las estructuras se dividen, fusionan y organizan en páginas. Dependiendo de la operación que desencadenó la construcción, el modelo de diseño de página puede o no renderizarse posteriormente en formato de página fija. Por ejemplo, calcular el número de páginas del documento o actualizar campos no requiere renderizado, mientras que la exportación a PDF sí lo requiere.

```cpp
enum class PageLayoutEvent
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | 0 | Valor predeterminado. |
| WatchDog | 1 | Corresponde a un punto de control en el código que se visita con frecuencia y que es adecuado para abortar el proceso. Mientras se está dentro de [Notify()](../ipagelayoutcallback/notify/) lance una excepción personalizada para abortar el proceso. Puede lanzar la excepción al manejar cualquier evento de devolución de llamada para abortar el proceso. Tenga en cuenta que si el proceso se aborta, el modelo de diseño de página queda en un estado indefinido. Sin embargo, si el proceso se aborta durante el reflujo de una página completa, debería ser posible usar el modelo de diseño hasta el final de esa página. |
| BuildStarted | 2 | La construcción del diseño de página ha comenzado. Se dispara una vez. Este es el primer evento que ocurre cuando se llama a [UpdatePageLayout](../../aspose.words/document/updatepagelayout/). |
| BuildFinished | 3 | La construcción del diseño de página ha finalizado. Se dispara una vez. Este es el último evento que ocurre cuando se llama a [UpdatePageLayout](../../aspose.words/document/updatepagelayout/). |
| ConversionStarted | 4 | La conversión del modelo de documento al diseño de página ha comenzado. Se dispara una vez. Esto ocurre cuando el modelo de diseño comienza a extraer el contenido del documento. |
| ConversionFinished | 5 | La conversión del modelo de documento al diseño de página ha finalizado. Se dispara una vez. Esto ocurre cuando el modelo de diseño deja de extraer el contenido del documento. |
| ReflowStarted | 6 | El reflujo del diseño de página ha comenzado. Se dispara una vez. Esto ocurre cuando el modelo de diseño comienza a reflujo del contenido del documento. |
| ReflowFinished | 7 | El reflujo del diseño de página ha finalizado. Se dispara una vez. Esto ocurre cuando el modelo de diseño deja de reflujo del contenido del documento. |
| PartReflowStarted | 8 | El reflujo de la página ha comenzado. Tenga en cuenta que la página puede reflujo varias veces y que el reflujo puede reiniciarse antes de terminar. |
| PartReflowFinished | 9 | El reflujo de la página ha finalizado. Tenga en cuenta que la página puede reflujo varias veces y que el reflujo puede reiniciarse antes de terminar. |
| PartRenderingStarted | 10 | [Rendering](../../aspose.words.rendering/) de la página ha comenzado. Esto se dispara una vez por página. |
| PartRenderingFinished | 11 | [Rendering](../../aspose.words.rendering/) de la página ha finalizado. Esto se dispara una vez por página. |

## Ver también

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
