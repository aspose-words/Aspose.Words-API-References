---
title: "Aspose::Words::Settings::ViewOptions::get_ZoomType método"
linktitle: "get_ZoomType"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Settings::ViewOptions::get_ZoomType método. Obtiene o establece un valor de zoom basado en el tamaño de la ventana en C++."
type: docs
weight: 7000
url: /es/cpp/aspose.words.settings/viewoptions/get_zoomtype/
---
## ViewOptions::get_ZoomType method


Obtiene o establece un valor de zoom basado en el tamaño de la ventana.

```cpp
Aspose::Words::Settings::ZoomType Aspose::Words::Settings::ViewOptions::get_ZoomType() const
```


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


Muestra cómo establecer un tipo de zoom personalizado, que las versiones anteriores de Microsoft Word aplicarán a un documento al cargarlo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// Establezca la propiedad \"ZoomType\" a \"ZoomType.PageWidth\" para obtener Microsoft Word
// para que el documento se amplíe automáticamente y se ajuste al ancho de la página.
// Establezca la propiedad \"ZoomType\" a \"ZoomType.FullPage\" para obtener Microsoft Word
// para que el documento se amplíe automáticamente y haga visible toda la primera página.
// Establezca la propiedad \"ZoomType\" a \"ZoomType.TextFit\" para obtener Microsoft Word
// para que el documento se amplíe automáticamente y se ajuste a los márgenes internos de texto de la primera página.
doc->get_ViewOptions()->set_ZoomType(zoomType);

doc->Save(get_ArtifactsDir() + u"ViewOptions.SetZoomType.doc");
```

## Ver también

* Enum [ZoomType](../../zoomtype/)
* Class [ViewOptions](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)
