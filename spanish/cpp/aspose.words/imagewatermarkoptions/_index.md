---
title: "Clase Aspose::Words::ImageWatermarkOptions"
linktitle: "ImageWatermarkOptions"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::ImageWatermarkOptions. Contiene opciones que pueden especificarse al agregar una marca de agua con imagen. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 34000
url: /es/cpp/aspose.words/imagewatermarkoptions/
---
## ImageWatermarkOptions class


Contiene opciones que pueden especificarse al agregar una marca de agua con imagen. Para obtener más información, visite el artículo de documentación [Working with Watermark](https://docs.aspose.com/words/cpp/working-with-watermark/).

```cpp
class ImageWatermarkOptions : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_IsWashout](./get_iswashout/)() const | Obtiene o establece un valor booleano que es responsable del efecto de desvanecimiento de la marca de agua. El valor predeterminado es **true**. |
| [get_Scale](./get_scale/)() const | Obtiene o establece el factor de escala expresado como una fracción de la imagen. El valor predeterminado es 0 - automático. |
| [GetType](./gettype/)() const override |  |
| [ImageWatermarkOptions](./imagewatermarkoptions/)() |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_IsWashout](./set_iswashout/)(bool) | Método setter para [Aspose::Words::ImageWatermarkOptions::get_IsWashout](./get_iswashout/). |
| [set_Scale](./set_scale/)(double) | Método setter para [Aspose::Words::ImageWatermarkOptions::get_Scale](./get_scale/). |
| static [Type](./type/)() |  |

## Ejemplos



Muestra cómo crear una marca de agua a partir de una imagen en el sistema de archivos local.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Modifique la apariencia de la marca de agua de imagen con un objeto ImageWatermarkOptions,
// luego páselo al crear una marca de agua a partir de un archivo de imagen.
auto imageWatermarkOptions = System::MakeObject<Aspose::Words::ImageWatermarkOptions>();
imageWatermarkOptions->set_Scale(5);
imageWatermarkOptions->set_IsWashout(false);

// Tenemos diferentes opciones para insertar una imagen.
// Utilice uno de los siguientes métodos para agregar una marca de agua de imagen.
doc->get_Watermark()->SetImage(System::Drawing::Image::FromFile(get_ImageDir() + u"Logo.jpg"));

doc->get_Watermark()->SetImage(System::Drawing::Image::FromFile(get_ImageDir() + u"Logo.jpg"), imageWatermarkOptions);

doc->get_Watermark()->SetImage(get_ImageDir() + u"Logo.jpg", imageWatermarkOptions);

doc->Save(get_ArtifactsDir() + u"Document.ImageWatermark.docx");
```

## Ver también

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
