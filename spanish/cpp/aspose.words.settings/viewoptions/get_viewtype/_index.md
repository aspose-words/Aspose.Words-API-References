---
title: "Método Aspose::Words::Settings::ViewOptions::get_ViewType"
linktitle: "get_ViewType"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Settings::ViewOptions::get_ViewType. Controla el modo de vista en Microsoft Word en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words.settings/viewoptions/get_viewtype/
---
## ViewOptions::get_ViewType method


Controla el modo de vista en Microsoft Word.

```cpp
Aspose::Words::Settings::ViewType Aspose::Words::Settings::ViewOptions::get_ViewType() const
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

* Enum [ViewType](../../viewtype/)
* Class [ViewOptions](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)
