---
title: "Aspose::Words::Settings::CompatibilityOptions::OptimizeFor método"
linktitle: "OptimizeFor"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Settings::CompatibilityOptions::OptimizeFor method. Permite optimizar el contenido del documento así como el comportamiento predeterminado de Aspose.Words a versiones particulares de MS Word. Use este método para evitar que MS Word muestre la cinta \"Compatibility mode\" al cargar el documento. (Nota que también puede necesitar establecer la propiedad Compliance a Iso29500_2008_Transitional o superior.) in C++."
type: docs
weight: 75000
url: /es/cpp/aspose.words.settings/compatibilityoptions/optimizefor/
---
## CompatibilityOptions::OptimizeFor method


Permite optimizar el contenido del documento así como el comportamiento predeterminado de Aspose.Words a versiones particulares de MS Word. Use este método para evitar que MS Word muestre la cinta "Compatibility mode" al cargar el documento. (Nota que también puede necesitar establecer la propiedad [Compliance](../../../aspose.words.saving/ooxmlsaveoptions/get_compliance/) a [Iso29500_2008_Transitional](../../../aspose.words.saving/ooxmlcompliance/) o superior.)

```cpp
void Aspose::Words::Settings::CompatibilityOptions::OptimizeFor(Aspose::Words::Settings::MsWordVersion version)
```


## Ejemplos



Muestra cómo establecer una especificación de cumplimiento OOXML a la que debe adherirse un documento guardado.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Si configuramos las opciones de compatibilidad para cumplir con Microsoft Word 2003,
// insertar una imagen definirá su forma usando VML.
doc->get_CompatibilityOptions()->OptimizeFor(Aspose::Words::Settings::MsWordVersion::Word2003);
builder->InsertImage(get_ImageDir() + u"Transparent background logo.png");

ASSERT_EQ(Aspose::Words::Drawing::ShapeMarkupLanguage::Vml, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_MarkupLanguage());

// El estándar OOXML "ISO/IEC 29500:2008" no admite formas VML.
// Si establecemos la propiedad "Compliance" del objeto SaveOptions a "OoxmlCompliance.Iso29500_2008_Strict",
// cualquier documento que guardemos pasando este objeto tendrá que seguir ese estándar.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Strict);
saveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Docx);

doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.Iso29500Strict.docx", saveOptions);

// Nuestro documento guardado define la forma usando DML para adherirse al estándar OOXML "ISO/IEC 29500:2008".
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OoxmlSaveOptions.Iso29500Strict.docx");

ASSERT_EQ(Aspose::Words::Drawing::ShapeMarkupLanguage::Dml, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_MarkupLanguage());
```


Muestra cómo alinear verticalmente el contenido de texto de un cuadro de texto.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 200, 200);

// Establezca la propiedad "VerticalAnchor" a "TextBoxAnchor.Top" para
// alinear el texto en este cuadro de texto con el lado superior de la forma.
// Establezca la propiedad "VerticalAnchor" a "TextBoxAnchor.Middle" para
// alinear el texto en este cuadro de texto al centro de la forma.
// Establezca la propiedad "VerticalAnchor" a "TextBoxAnchor.Bottom" para
// alinear el texto en este cuadro de texto a la parte inferior de la forma.
shape->get_TextBox()->set_VerticalAnchor(verticalAnchor);

builder->MoveTo(shape->get_FirstParagraph());
builder->Write(u"Hello world!");

// La alineación vertical del texto dentro de los cuadros de texto está disponible a partir de Microsoft Word 2007.
doc->get_CompatibilityOptions()->OptimizeFor(Aspose::Words::Settings::MsWordVersion::Word2007);
doc->Save(get_ArtifactsDir() + u"Shape.VerticalAnchor.docx");
```

## Ver también

* Enum [MsWordVersion](../../mswordversion/)
* Class [CompatibilityOptions](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)
