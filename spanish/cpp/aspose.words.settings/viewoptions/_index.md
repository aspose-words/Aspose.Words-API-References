---
title: "Aspose::Words::Settings::ViewOptions clase"
linktitle: "ViewOptions"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::Settings::ViewOptions. Proporciona varias opciones que controlan cómo se muestra un documento en Microsoft Word. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 9000
url: /es/cpp/aspose.words.settings/viewoptions/
---
## ViewOptions class


Proporciona varias opciones que controlan cómo se muestra un documento en Microsoft Word. Para obtener más información, visite el artículo de documentación [Work with Options and Appearance of Word Documents](https://docs.aspose.com/words/cpp/work-with-word-document-options-and-appearance/).

```cpp
class ViewOptions : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_DisplayBackgroundShape](./get_displaybackgroundshape/)() const | Controla la visualización de la forma de fondo en la vista de diseño de impresión. |
| [get_DoNotDisplayPageBoundaries](./get_donotdisplaypageboundaries/)() const | Desactiva la visualización del espacio entre la parte superior del texto y el borde superior de la página. |
| [get_FormsDesign](./get_formsdesign/)() const | Especifica si el documento está en modo de diseño de formularios. |
| [get_ViewType](./get_viewtype/)() const | Controla el modo de vista en Microsoft Word. |
| [get_ZoomPercent](./get_zoompercent/)() const | Obtiene o establece el porcentaje al que desea ver su documento. |
| [get_ZoomType](./get_zoomtype/)() const | Obtiene o establece un valor de zoom basado en el tamaño de la ventana. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_DisplayBackgroundShape](./set_displaybackgroundshape/)(bool) | Método set para [Aspose::Words::Settings::ViewOptions::get_DisplayBackgroundShape](./get_displaybackgroundshape/). |
| [set_DoNotDisplayPageBoundaries](./set_donotdisplaypageboundaries/)(bool) | Método set para [Aspose::Words::Settings::ViewOptions::get_DoNotDisplayPageBoundaries](./get_donotdisplaypageboundaries/). |
| [set_FormsDesign](./set_formsdesign/)(bool) | Método set para [Aspose::Words::Settings::ViewOptions::get_FormsDesign](./get_formsdesign/). |
| [set_ViewType](./set_viewtype/)(Aspose::Words::Settings::ViewType) | Método set para [Aspose::Words::Settings::ViewOptions::get_ViewType](./get_viewtype/). |
| [set_ZoomPercent](./set_zoompercent/)(int32_t) | Método set para [Aspose::Words::Settings::ViewOptions::get_ZoomPercent](./get_zoompercent/). |
| [set_ZoomType](./set_zoomtype/)(Aspose::Words::Settings::ZoomType) | Método set para [Aspose::Words::Settings::ViewOptions::get_ZoomType](./get_zoomtype/). |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
