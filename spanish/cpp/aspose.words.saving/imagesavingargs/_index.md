---
title: "Aspose::Words::Saving::ImageSavingArgs class"
linktitle: "ImageSavingArgs"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::ImageSavingArgs class. Proporciona datos para el evento ImageSaving(). Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 12000
url: /es/cpp/aspose.words.saving/imagesavingargs/
---
## ImageSavingArgs class


Proporciona datos para el evento [ImageSaving()](../iimagesavingcallback/imagesaving/). Para obtener más información, visite el artículo de documentación [Save a Document](https://docs.aspose.com/words/cpp/save-a-document/).

```cpp
class ImageSavingArgs : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_CurrentShape](./get_currentshape/)() const | Obtiene el objeto [ShapeBase](../../aspose.words.drawing/shapebase/) correspondiente a la forma o forma de grupo que está a punto de guardarse. |
| [get_Document](./get_document/)() | Obtiene el objeto documento que se está guardando actualmente. |
| [get_ImageFileName](./get_imagefilename/)() const | Obtiene o establece el nombre de archivo (sin ruta) donde se guardará la imagen. |
| [get_ImageStream](./get_imagestream/)() const | Permite especificar el flujo donde se guardará la imagen. |
| [get_IsImageAvailable](./get_isimageavailable/)() const | Devuelve **true** si la imagen actual está disponible para exportar. |
| [get_KeepImageStreamOpen](./get_keepimagestreamopen/)() const | Especifica si Aspose.Words debe mantener el flujo abierto o cerrarlo después de guardar una imagen. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_ImageFileName](./set_imagefilename/)(const System::String\&) | Setter para [Aspose::Words::Saving::ImageSavingArgs::get_ImageFileName](./get_imagefilename/). |
| [set_ImageStream](./set_imagestream/)(const System::SharedPtr\<System::IO::Stream\>\&) | Método set para [Aspose::Words::Saving::ImageSavingArgs::get_ImageStream](./get_imagestream/). |
| [set_ImageStream](./set_imagestream/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| [set_KeepImageStreamOpen](./set_keepimagestreamopen/)(bool) | Método set para [Aspose::Words::Saving::ImageSavingArgs::get_KeepImageStreamOpen](./get_keepimagestreamopen/). |
| static [Type](./type/)() |  |
## Observaciones


De forma predeterminada, cuando Aspose.Words guarda un documento en HTML, guarda cada imagen en un archivo separado. Aspose.Words utiliza el nombre del archivo del documento y un número único para generar un nombre de archivo único para cada imagen encontrada en el documento.

[ImageSavingArgs](./) allows to redefine how image file names are generated or to completely circumvent saving of images into files by providing your own stream objects.

Para aplicar su propia lógica para generar nombres de archivo de imagen, use las propiedades [ImageFileName](./get_imagefilename/), [CurrentShape](./get_currentshape/) y [IsImageAvailable](./get_isimageavailable/).

Para guardar imágenes en flujos en lugar de archivos, use la propiedad [ImageStream](./get_imagestream/).
## Ver también

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
