---
title: "Aspose::Words::Drawing::ImageType enum"
linktitle: "ImageType"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::ImageType enum. Especifica el tipo (formato) de una imagen en un documento Microsoft Word en C++."
type: docs
weight: 28000
url: /es/cpp/aspose.words.drawing/imagetype/
---
## ImageType enum


Especifica el tipo (formato) de una imagen en un documento de Microsoft Word.

```cpp
enum class ImageType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| NoImage | 0 | No hay datos de imagen. |
| Desconocido | 1 | Un tipo de imagen desconocido o un tipo de imagen que no puede almacenarse directamente dentro de un documento Microsoft Word. |
| Emf | 2 | Metarchivo mejorado de Windows. |
| Wmf | 3 | Metarchivo de Windows. |
| Pict | 4 | Macintosh PICT. Una imagen existente se conservará en un documento, pero la inserción de nuevas imágenes PICT en un documento no es compatible. |
| Jpeg | 5 | JPEG JFIF. |
| Png | 6 | Gráficos de Red Portátiles. |
| Bmp | 7 | Bitmap de Windows. |
| Eps | 8 | PostScript encapsulado. |
| WebP | 9 | WebP. |
| Gif | 10 | GIF. |


## Ejemplos



Muestra cómo agregar una imagen a una forma y comprobar su tipo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> imgShape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
ASSERT_EQ(Aspose::Words::Drawing::ImageType::Jpeg, imgShape->get_ImageData()->get_ImageType());
```

## Ver también

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
