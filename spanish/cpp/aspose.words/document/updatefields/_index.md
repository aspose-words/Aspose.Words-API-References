---
title: "Aspose::Words::Document::UpdateFields método"
linktitle: "UpdateFields"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Document::UpdateFields método. Actualiza los valores de los campos en todo el documento en C++."
type: docs
weight: 96000
url: /es/cpp/aspose.words/document/updatefields/
---
## Document::UpdateFields method


Actualiza los valores de los campos en todo el documento.

```cpp
void Aspose::Words::Document::UpdateFields()
```

## Observaciones


Cuando abres, modificas y luego guardas un documento, Aspose.Words no actualiza los campos automáticamente, los mantiene intactos. Por lo tanto, normalmente querrías llamar a este método antes de guardar si has modificado el documento programáticamente y deseas asegurarte de que los valores de campo correctos (calculados) aparezcan en el documento guardado.

No es necesario actualizar los campos después de ejecutar una combinación de correspondencia porque la combinación de correspondencia es un tipo de actualización de campos y actualiza automáticamente todos los campos del documento.

Este método no actualiza todos los tipos de campos. Para la lista detallada de tipos de campos compatibles, consulta la Guía del Programador.

Este método no actualiza los campos que están relacionados con los algoritmos de diseño de página (p. ej., PAGE, PAGES, PAGEREF). Los campos relacionados con el diseño de página se actualizan cuando renderizas un documento o llamas a [UpdatePageLayout](../updatepagelayout/).

Utiliza el método [NormalizeFieldTypes](../normalizefieldtypes/) antes de actualizar los campos si hubo cambios en el documento que afectaron los tipos de campos.

Para actualizar los campos en una parte específica del documento, usa [UpdateFields](../../range/updatefields/).

## Ejemplos



Muestra cómo insertar una tabla de contenido (TOC) en un documento usando estilos de encabezado como entradas.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserta una tabla de contenido para la primera página del documento.
// Configura la tabla para que incluya párrafos con encabezados de niveles 1 a 3.
// Además, configura sus entradas para que sean hipervínculos que nos llevarán
// a la ubicación del encabezado al hacer clic izquierdo en Microsoft Word.
builder->InsertTableOfContents(u"\\o \"1-3\" \\h \\z \\u");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// Poblar el índice añadiendo párrafos con estilos de encabezado.
// Cada encabezado de este tipo con un nivel entre 1 y 3 creará una entrada en el índice.
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);
builder->Writeln(u"Heading 1");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);
builder->Writeln(u"Heading 1.1");
builder->Writeln(u"Heading 1.2");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);
builder->Writeln(u"Heading 2");
builder->Writeln(u"Heading 3");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);
builder->Writeln(u"Heading 3.1");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading3);
builder->Writeln(u"Heading 3.1.1");
builder->Writeln(u"Heading 3.1.2");
builder->Writeln(u"Heading 3.1.3");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading4);
builder->Writeln(u"Heading 3.1.3.1");
builder->Writeln(u"Heading 3.1.3.2");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);
builder->Writeln(u"Heading 3.2");
builder->Writeln(u"Heading 3.3");

// Un índice es un campo de un tipo que necesita actualizarse para mostrar un resultado actualizado.
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertToc.docx");
```


Muestra cómo usar el campo QUOTE.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserte un campo QUOTE, que mostrará el valor de su propiedad Text.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldQuote>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldQuote, true));
field->set_Text(u"\"Quoted text\"");

ASSERT_EQ(u" QUOTE  \"\\\"Quoted text\\\"\"", field->GetFieldCode());

// Inserte un campo QUOTE y anide dentro de él un campo DATE.
// Los campos DATE actualizan su valor a la fecha actual cada vez que abrimos el documento usando Microsoft Word.
// Anidar el campo DATE dentro del campo QUOTE de esta manera congelará su valor
// a la fecha en que creamos el documento.
builder->Write(u"\nDocument creation date: ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldQuote>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldQuote, true));
builder->MoveTo(field->get_Separator());
builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true);

ASSERT_EQ(System::String(u" QUOTE \u0013 DATE \u0014") + System::DateTime::get_Now().get_Date().ToShortDateString() + u"\u0015", field->GetFieldCode());

// Actualice todos los campos para que muestren sus resultados correctos.
doc->UpdateFields();

ASSERT_EQ(u"\"Quoted text\"", doc->get_Range()->get_Fields()->idx_get(0)->get_Result());

doc->Save(get_ArtifactsDir() + u"Field.QUOTE.docx");
```


Muestra cómo establecer los detalles del usuario y mostrarlos usando campos.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Cree un objeto UserInformation y configúrelo como la fuente de datos para los campos que muestran información del usuario.
auto userInformation = System::MakeObject<Aspose::Words::Fields::UserInformation>();
userInformation->set_Name(u"John Doe");
userInformation->set_Initials(u"J. D.");
userInformation->set_Address(u"123 Main Street");
doc->get_FieldOptions()->set_CurrentUser(userInformation);

// Inserte los campos USERNAME, USERINITIALS y USERADDRESS, que muestran valores de
// las respectivas propiedades del objeto UserInformation que hemos creado arriba.
ASSERT_EQ(userInformation->get_Name(), builder->InsertField(u" USERNAME ")->get_Result());
ASSERT_EQ(userInformation->get_Initials(), builder->InsertField(u" USERINITIALS ")->get_Result());
ASSERT_EQ(userInformation->get_Address(), builder->InsertField(u" USERADDRESS ")->get_Result());

// El objeto field options también tiene un usuario predeterminado estático al que los campos de todos los documentos pueden referirse.
Aspose::Words::Fields::UserInformation::get_DefaultUser()->set_Name(u"Default User");
Aspose::Words::Fields::UserInformation::get_DefaultUser()->set_Initials(u"D. U.");
Aspose::Words::Fields::UserInformation::get_DefaultUser()->set_Address(u"One Microsoft Way");
doc->get_FieldOptions()->set_CurrentUser(Aspose::Words::Fields::UserInformation::get_DefaultUser());

ASSERT_EQ(u"Default User", builder->InsertField(u" USERNAME ")->get_Result());
ASSERT_EQ(u"D. U.", builder->InsertField(u" USERINITIALS ")->get_Result());
ASSERT_EQ(u"One Microsoft Way", builder->InsertField(u" USERADDRESS ")->get_Result());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"FieldOptions.CurrentUser.docx");
```

## Ver también

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
