---
title: "Método Aspose::Words::DocumentBase::get_BackgroundShape"
linktitle: "get_BackgroundShape"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::DocumentBase::get_BackgroundShape. Obtiene o establece la forma de fondo del documento. Puede ser nulo en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words/documentbase/get_backgroundshape/
---
## DocumentBase::get_BackgroundShape method


Obtiene o establece la forma de fondo del documento. Puede ser **null**.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBase::get_BackgroundShape() const
```

## Observaciones


Microsoft Word solo permite una forma cuya propiedad [ShapeType](../../../aspose.words.drawing/shapebase/get_shapetype/) sea igual a [Rectangle](../../../aspose.words.drawing/shapetype/) para usarse como forma de fondo de un documento.

Microsoft Word solo admite las propiedades de relleno de una forma de fondo. Todas las demás propiedades se ignoran.

Establecer esta propiedad a un valor no nulo también configurará [DisplayBackgroundShape](../../../aspose.words.settings/viewoptions/get_displaybackgroundshape/) a **true**.

## Ejemplos



Muestra cómo establecer una forma de fondo para cada página de un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

ASSERT_TRUE(System::TestTools::IsNull(doc->get_BackgroundShape()));

// El único tipo de forma que podemos usar como fondo es un rectángulo.
auto shapeRectangle = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);

// Hay dos formas de usar esta forma como fondo de página.
// 1 -  Un color sólido:
shapeRectangle->set_FillColor(System::Drawing::Color::get_LightBlue());
doc->set_BackgroundShape(shapeRectangle);

doc->Save(get_ArtifactsDir() + u"DocumentBase.BackgroundShape.FlatColor.docx");

// 2 -  Una imagen:
shapeRectangle = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
shapeRectangle->get_ImageData()->SetImage(get_ImageDir() + u"Transparent background logo.png");

// Ajusta la apariencia de la imagen para que sea más adecuada como marca de agua.
shapeRectangle->get_ImageData()->set_Contrast(0.2);
shapeRectangle->get_ImageData()->set_Brightness(0.7);

doc->set_BackgroundShape(shapeRectangle);

ASSERT_TRUE(doc->get_BackgroundShape()->get_HasImage());

auto saveOptions = System::MakeObject<Aspose::Words::Saving::PdfSaveOptions>();
saveOptions->set_CacheBackgroundGraphics(false);

// Microsoft Word no admite formas con imágenes como fondos,
// pero aún podemos ver estos fondos en otros formatos de guardado como .pdf.
doc->Save(get_ArtifactsDir() + u"DocumentBase.BackgroundShape.Image.pdf", saveOptions);
```

## Ver también

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
