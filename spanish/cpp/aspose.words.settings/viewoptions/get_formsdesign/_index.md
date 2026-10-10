---
title: "Método Aspose::Words::Settings::ViewOptions::get_FormsDesign"
linktitle: "get_FormsDesign"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Settings::ViewOptions::get_FormsDesign. Especifica si el documento está en modo de diseño de formularios en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words.settings/viewoptions/get_formsdesign/
---
## ViewOptions::get_FormsDesign method


Especifica si el documento está en modo de diseño de formularios.

```cpp
bool Aspose::Words::Settings::ViewOptions::get_FormsDesign() const
```

## Observaciones


Actualmente funciona solo con documentos en formato WordML.

## Ejemplos



Muestra cómo habilitar/deshabilitar el modo de diseño de formularios.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// Establezca la propiedad "FormsDesign" a "false" para mantener deshabilitado el modo de diseño de formularios.
// Establezca la propiedad "FormsDesign" a "true" para habilitar el modo de diseño de formularios.
doc->get_ViewOptions()->set_FormsDesign(useFormsDesign);

doc->Save(get_ArtifactsDir() + u"ViewOptions.FormsDesign.xml");

ASPOSE_ASSERT_EQ(useFormsDesign, System::IO::File::ReadAllText(get_ArtifactsDir() + u"ViewOptions.FormsDesign.xml").Contains(u"<w:formsDesign />"));
```

## Ver también

* Class [ViewOptions](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)
