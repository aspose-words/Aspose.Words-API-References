---
title: "Aspose::Words::Drawing::ShapeBase::get_IsImage método"
linktitle: "get_IsImage"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::ShapeBase::get_IsImage método. Devuelve true si esta forma es una forma de imagen en C++."
type: docs
weight: 29000
url: /es/cpp/aspose.words.drawing/shapebase/get_isimage/
---
## ShapeBase::get_IsImage method


Devuelve **true** si esta forma es una forma de imagen.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_IsImage()
```


## Ejemplos



Muestra cómo abrir un documento HTML con imágenes desde un flujo usando un URI base.
```cpp
{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_MyDir() + u"Document.html");
    // Pase el URI de la carpeta base al cargarlo
    // para que cualquier imagen con URIs relativos en el documento HTML pueda ser encontrada.
    auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
    loadOptions->set_BaseUri(get_ImageDir());

    auto doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);

    // Verifique que la primera forma del documento contenga una imagen válida.
    auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

    ASSERT_TRUE(shape->get_IsImage());
    ASSERT_FALSE(System::TestTools::IsNull(shape->get_ImageData()->get_ImageBytes()));
    ASSERT_NEAR(32.0, Aspose::Words::ConvertUtil::PointToPixel(shape->get_Width()), 0.01);
    ASSERT_NEAR(32.0, Aspose::Words::ConvertUtil::PointToPixel(shape->get_Height()), 0.01);
}
```

## Ver también

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
