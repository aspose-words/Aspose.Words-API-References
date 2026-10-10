---
title: "Aspose::Words::Document::get_ViewOptions método"
linktitle: "get_ViewOptions"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Document::get_ViewOptions. Proporciona opciones para controlar cómo se muestra el documento en Microsoft Word en C++."
type: docs
weight: 58000
url: /es/cpp/aspose.words/document/get_viewoptions/
---
## Document::get_ViewOptions method


Proporciona opciones para controlar cómo se muestra el documento en Microsoft Word.

```cpp
System::SharedPtr<Aspose::Words::Settings::ViewOptions> Aspose::Words::Document::get_ViewOptions()
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

* Class [ViewOptions](../../../aspose.words.settings/viewoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
