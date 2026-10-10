---
title: "Aspose::Words::Drawing::ImageData::get_SourceFullName método"
linktitle: "get_SourceFullName"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::ImageData::get_SourceFullName método. Obtiene o establece la ruta y el nombre del archivo fuente para la imagen vinculada en C++."
type: docs
weight: 18000
url: /es/cpp/aspose.words.drawing/imagedata/get_sourcefullname/
---
## ImageData::get_SourceFullName method


Obtiene o establece la ruta y el nombre del archivo fuente para la imagen vinculada.

```cpp
System::String Aspose::Words::Drawing::ImageData::get_SourceFullName()
```

## Observaciones


El valor predeterminado es una cadena vacía.

Si [SourceFullName](./) no es una cadena vacía, la imagen está vinculada.

## Ejemplos



Muestra cómo insertar una imagen enlazada en un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::String imageFileName = get_ImageDir() + u"Windows MetaFile.wmf";

// A continuación se presentan dos formas de aplicar una imagen a una forma para que pueda mostrarla.
// 1 -  Configure la forma para que contenga la imagen.
auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(builder->get_Document(), Aspose::Words::Drawing::ShapeType::Image);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::Inline);
shape->get_ImageData()->SetImage(imageFileName);

builder->InsertNode(shape);

doc->Save(get_ArtifactsDir() + u"Image.CreateLinkedImage.Embedded.docx");

// Cada imagen que almacenemos en la forma aumentará el tamaño de nuestro documento.
ASSERT_TRUE(70000 < System::MakeObject<System::IO::FileInfo>(get_ArtifactsDir() + u"Image.CreateLinkedImage.Embedded.docx")->get_Length());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->RemoveAllChildren();

// 2 -  Configure la forma para enlazar a un archivo de imagen en el sistema de archivos local.
shape = System::MakeObject<Aspose::Words::Drawing::Shape>(builder->get_Document(), Aspose::Words::Drawing::ShapeType::Image);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::Inline);
shape->get_ImageData()->set_SourceFullName(imageFileName);

builder->InsertNode(shape);
doc->Save(get_ArtifactsDir() + u"Image.CreateLinkedImage.Linked.docx");

// Enlazar imágenes ahorrará espacio y resultará en un documento más pequeño.
// Sin embargo, el documento solo puede mostrar la imagen correctamente mientras
// el archivo de imagen está presente en la ubicación a la que apunta la propiedad "SourceFullName" de la forma.
ASSERT_TRUE(10000 > System::MakeObject<System::IO::FileInfo>(get_ArtifactsDir() + u"Image.CreateLinkedImage.Linked.docx")->get_Length());
```

## Ver también

* Class [ImageData](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
