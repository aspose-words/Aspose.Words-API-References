---
title: "Aspose::Words::Drawing::ImageData::get_IsLink método"
linktitle: "get_IsLink"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::ImageData::get_IsLink método. Devuelve **true** si la imagen está vinculada a la forma (cuando se especifica SourceFullName) en C++."
type: docs
weight: 16000
url: /es/cpp/aspose.words.drawing/imagedata/get_islink/
---
## ImageData::get_IsLink method


Devuelve **true** si la imagen está vinculada a la forma (cuando se especifica [SourceFullName](../get_sourcefullname/)).

```cpp
bool Aspose::Words::Drawing::ImageData::get_IsLink()
```


## Ejemplos



Muestra cómo editar los datos de imagen de una forma.
```cpp
auto imgSourceDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");
auto sourceShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(imgSourceDoc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->idx_get(0));

auto dstDoc = System::MakeObject<Aspose::Words::Document>();

// Importe una forma del documento fuente y añádala al primer párrafo.
auto importedShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(dstDoc->ImportNode(sourceShape, true));
dstDoc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(importedShape);

// La forma importada contiene una imagen. Podemos acceder a las propiedades de la imagen y a los datos sin procesar mediante el objeto ImageData.
System::SharedPtr<Aspose::Words::Drawing::ImageData> imageData = importedShape->get_ImageData();
imageData->set_Title(u"Imported Image");

ASSERT_TRUE(imageData->get_HasImage());

// Si una imagen no tiene bordes, su objeto ImageData definirá el color del borde como vacío.
ASSERT_EQ(4, imageData->get_Borders()->get_Count());
ASPOSE_ASSERT_EQ(System::Drawing::Color::Empty, imageData->get_Borders()->idx_get(0)->get_Color());

// Esta imagen no está vinculada a otra forma o archivo de imagen en el sistema de archivos local.
ASSERT_FALSE(imageData->get_IsLink());
ASSERT_FALSE(imageData->get_IsLinkOnly());

// Las propiedades "Brightness" y "Contrast" definen el brillo y el contraste de la imagen
// en una escala de 0 a 1, con el valor predeterminado en 0.5.
imageData->set_Brightness(0.8);
imageData->set_Contrast(1.0);

// Los valores de brillo y contraste anteriores han creado una imagen con mucho blanco.
// Podemos seleccionar un color con la propiedad ChromaKey para reemplazarlo por transparencia, como el blanco.
imageData->set_ChromaKey(System::Drawing::Color::get_White());

// Importe nuevamente la forma fuente y establezca la imagen en monocromo.
importedShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(dstDoc->ImportNode(sourceShape, true));
dstDoc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(importedShape);

importedShape->get_ImageData()->set_GrayScale(true);

// Importe nuevamente la forma fuente para crear una tercera imagen y configúrela en BiLevel.
// BiLevel establece cada píxel en negro o blanco, según cuál esté más cerca del color original.
importedShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(dstDoc->ImportNode(sourceShape, true));
dstDoc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(importedShape);

importedShape->get_ImageData()->set_BiLevel(true);

// El recorte se determina en una escala de 0-1. Recortar un lado en 0.3
// recortará el 30% de la imagen en el lado recortado.
importedShape->get_ImageData()->set_CropBottom(0.3);
importedShape->get_ImageData()->set_CropLeft(0.3);
importedShape->get_ImageData()->set_CropTop(0.3);
importedShape->get_ImageData()->set_CropRight(0.3);

dstDoc->Save(get_ArtifactsDir() + u"Drawing.ImageData.docx");
```

## Ver también

* Class [ImageData](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
