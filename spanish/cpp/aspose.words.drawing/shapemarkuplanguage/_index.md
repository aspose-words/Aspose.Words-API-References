---
title: "Enumeración Aspose::Words::Drawing::ShapeMarkupLanguage"
linktitle: "ShapeMarkupLanguage"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Enumeración Aspose::Words::Drawing::ShapeMarkupLanguage. Especifica el lenguaje de marcado usado para la forma en C++."
type: docs
weight: 37000
url: /es/cpp/aspose.words.drawing/shapemarkuplanguage/
---
## ShapeMarkupLanguage enum


Especifica el lenguaje [Markup](../../aspose.words.markup/) usado para la forma.

```cpp
enum class ShapeMarkupLanguage : uint8_t
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Dml | 0 | [Drawing](../)[Markup](../../aspose.words.markup/) Language se utiliza para definir la forma. |
| Vml | 1 | Vector [Markup](../../aspose.words.markup/) Language se usa para definir la forma. |


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

## Ver también

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
