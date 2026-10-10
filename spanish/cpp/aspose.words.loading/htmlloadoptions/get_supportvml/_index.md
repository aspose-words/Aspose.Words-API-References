---
title: "Aspose::Words::Loading::HtmlLoadOptions::get_SupportVml método"
linktitle: "get_SupportVml"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Loading::HtmlLoadOptions::get_SupportVml método. Obtiene o establece un valor que indica si se admiten imágenes VML en C++."
type: docs
weight: 7000
url: /es/cpp/aspose.words.loading/htmlloadoptions/get_supportvml/
---
## HtmlLoadOptions::get_SupportVml method


Obtiene o establece un valor que indica si se deben admitir imágenes VML.

```cpp
bool Aspose::Words::Loading::HtmlLoadOptions::get_SupportVml() const
```


## Ejemplos



Muestra cómo admitir comentarios condicionales al cargar un documento HTML.
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>();

// Si el valor es verdadero, entonces tenemos en cuenta el código VML al analizar el documento cargado.
loadOptions->set_SupportVml(supportVml);

// Este documento contiene una imagen JPEG dentro de las etiquetas \"<!--[if gte vml 1]>\" ,
// y una imagen PNG diferente dentro de las etiquetas \"<![if !vml]>\".
// Si establecemos la bandera \"SupportVml\" a \"true\", entonces Aspose.Words cargará el JPEG.
// Si establecemos esta bandera a \"false\", entonces Aspose.Words solo cargará el PNG.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"VML conditional.htm", loadOptions);

if (supportVml)
{
    ASSERT_EQ(Aspose::Words::Drawing::ImageType::Jpeg, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_ImageData()->get_ImageType());
}
else
{
    ASSERT_EQ(Aspose::Words::Drawing::ImageType::Png, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_ImageData()->get_ImageType());
}
```

## Ver también

* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
