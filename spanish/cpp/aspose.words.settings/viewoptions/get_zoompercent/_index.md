---
title: "Aspose::Words::Settings::ViewOptions::get_ZoomPercent método"
linktitle: "get_ZoomPercent"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Settings::ViewOptions::get_ZoomPercent método. Obtiene o establece el porcentaje al que desea ver su documento en C++."
type: docs
weight: 6000
url: /es/cpp/aspose.words.settings/viewoptions/get_zoompercent/
---
## ViewOptions::get_ZoomPercent method


Obtiene o establece el porcentaje al que desea ver su documento.

```cpp
int32_t Aspose::Words::Settings::ViewOptions::get_ZoomPercent() const
```

## Observaciones


Aunque Aspose.Words puede leer y escribir esta opción, su uso es específico de la aplicación. Por ejemplo, MS Word 2013 no respeta el valor de esta opción.

## Ejemplos



Muestra cómo establecer un factor de zoom personalizado, que las versiones anteriores de Microsoft Word aplicarán a un documento al cargarlo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

doc->get_ViewOptions()->set_ViewType(Aspose::Words::Settings::ViewType::PageLayout);
doc->get_ViewOptions()->set_ZoomPercent(50);

ASSERT_EQ(Aspose::Words::Settings::ZoomType::Custom, doc->get_ViewOptions()->get_ZoomType());
ASSERT_EQ(Aspose::Words::Settings::ZoomType::None, doc->get_ViewOptions()->get_ZoomType());

doc->Save(get_ArtifactsDir() + u"ViewOptions.SetZoomPercentage.doc");
```

## Ver también

* Class [ViewOptions](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)
