---
title: "Método Aspose::Words::Loading::LoadOptions::get_BaseUri"
linktitle: "get_BaseUri"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Loading::LoadOptions::get_BaseUri. Obtiene o establece la cadena que se utilizará para resolver URIs relativos encontrados en el documento en URIs absolutos cuando sea necesario. Puede ser nulo o una cadena vacía. El valor predeterminado es null en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.loading/loadoptions/get_baseuri/
---
## LoadOptions::get_BaseUri method


Obtiene o establece la cadena que se usará para resolver URIs relativos encontrados en el documento a URIs absolutos cuando sea necesario. Puede ser **null** o una cadena vacía. El valor predeterminado es **null**.

```cpp
System::String Aspose::Words::Loading::LoadOptions::get_BaseUri() const
```

## Observaciones


Esta propiedad se usa para resolver URIs relativos en absolutos en los siguientes casos:

1. Al cargar un documento HTML desde un flujo y el documento contiene imágenes con URIs relativos y no tiene un URI base especificado en el elemento BASE del HTML.
1. Al guardar un documento en PDF y otros formatos, para recuperar imágenes vinculadas mediante URIs relativos de modo que las imágenes puedan guardarse en el documento de salida.



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

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
