---
title: "Aspose::Words::Saving::DownsampleOptions class"
linktitle: "DownsampleOptions"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::DownsampleOptions class. Permite especificar opciones de submuestreo. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 6000
url: /es/cpp/aspose.words.saving/downsampleoptions/
---
## DownsampleOptions class


Permite especificar opciones de submuestreo. Para obtener más información, visite el artículo de documentación [Guardar un documento](https://docs.aspose.com/words/cpp/save-a-document/).

```cpp
class DownsampleOptions : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [DownsampleOptions](./downsampleoptions/)() |  |
| [get_DownsampleImages](./get_downsampleimages/)() const | Especifica si las imágenes deben ser submuestreadas. |
| [get_Resolution](./get_resolution/)() const | Especifica la resolución en píxeles por pulgada a la que deben submuestrearse las imágenes. |
| [get_ResolutionThreshold](./get_resolutionthreshold/)() const | Especifica la resolución umbral en píxeles por pulgada. Si la resolución de una imagen en el documento es inferior al valor umbral, el algoritmo de submuestreo no se aplicará. Un valor de 0 indica que la verificación de umbral no se utiliza y todas las imágenes que pueden reducirse de tamaño son submuestreadas. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_DownsampleImages](./set_downsampleimages/)(bool) | Especifica si las imágenes deben ser submuestreadas. |
| [set_Resolution](./set_resolution/)(int32_t) | Especifica la resolución en píxeles por pulgada a la que deben submuestrearse las imágenes. |
| [set_ResolutionThreshold](./set_resolutionthreshold/)(int32_t) | Método setter para [Aspose::Words::Saving::DownsampleOptions::get_ResolutionThreshold](./get_resolutionthreshold/). |
| static [Type](./type/)() |  |
## Ver también

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
