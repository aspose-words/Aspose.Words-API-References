---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ScaleImageToShapeSize método"
linktitle: "get_ScaleImageToShapeSize"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ScaleImageToShapeSize método. Especifica si las imágenes son escaladas por Aspose.Words al tamaño de la forma contenedora al exportar a HTML, MHTML o EPUB. El valor predeterminado es true en C++."
type: docs
weight: 46000
url: /es/cpp/aspose.words.saving/htmlsaveoptions/get_scaleimagetoshapesize/
---
## HtmlSaveOptions::get_ScaleImageToShapeSize method


Especifica si las imágenes son escaladas por Aspose.Words al tamaño de la forma contenedora al exportar a HTML, MHTML o EPUB. El valor predeterminado es **true**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ScaleImageToShapeSize() const
```

## Observaciones


Una imagen en un documento de Microsoft Word es una forma. La forma tiene un tamaño y la imagen tiene su propio tamaño. Los tamaños no están vinculados directamente. Por ejemplo, la imagen puede ser de 1024x786 píxeles, pero la forma que muestra esta imagen puede ser de 400x300 puntos.

Para mostrar una imagen en el navegador, debe escalarse al tamaño de la forma. La propiedad [ScaleImageToShapeSize](./) controla dónde se realiza el escalado de la imagen: en Aspose.Words durante la exportación a HTML o en el navegador al mostrar el documento.

Cuando [ScaleImageToShapeSize](./) es **true**, la imagen es escalada por [Aspose.Words](../../../aspose.words/) usando un escalado de alta calidad durante la exportación a HTML. Cuando [ScaleImageToShapeSize](./) es **false**, la imagen se exporta con su tamaño original y el navegador debe escalarla.

En general, los navegadores realizan un escalado rápido y de baja calidad. Como resultado, normalmente obtendrá una mejor calidad de visualización en el navegador y un tamaño de archivo menor cuando [ScaleImageToShapeSize](./) es **true**, pero una mejor calidad de impresión y una conversión más rápida cuando [ScaleImageToShapeSize](./) es **false**.

In addition to shapes containing individual raster images, this option also affects group shapes consisting of raster images. If [ScaleImageToShapeSize](./) is **false** and a group shape contains raster images whose intrinsic resolution is higher than the value specified in [ImageResolution](../get_imageresolution/), Aspose.Words will increase rendering resolution for that group. This allows to better preserve quality of grouped high resolution images when saving to HTML.

## Ver también

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
