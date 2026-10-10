---
title: "Aspose::Words::DocumentBuilder::InsertTableOfContents method"
linktitle: "InsertTableOfContents"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::DocumentBuilder::InsertTableOfContents method. Inserta un campo TOC (tabla de contenido) en el documento en C++."
type: docs
weight: 48000
url: /es/cpp/aspose.words/documentbuilder/inserttableofcontents/
---
## DocumentBuilder::InsertTableOfContents method


Inserta un campo TOC (tabla de contenido) en el documento.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::DocumentBuilder::InsertTableOfContents(const System::String &switches)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| conmutadores | const System::String\& | Los conmutadores del campo TOC. |
## Observaciones


Este método inserta un campo TOC (tabla de contenido) en el documento en la posición actual.

Una tabla de contenido en un documento Word puede construirse de varias maneras y formatearse usando una variedad de opciones. La forma en que la tabla se construye y muestra en Microsoft Word está controlada por los conmutadores del campo.

La forma más fácil de especificar los conmutadores es insertar y configurar una tabla de contenido en un documento Word usando el menú Insert->Reference->Index y [Tables](../../../aspose.words.tables/) , luego activar la visualización de códigos de campo para ver los conmutadores. Puedes pulsar Alt+F9 en Microsoft Word para alternar la visualización de los códigos de campo encendida o apagada.

Por ejemplo, después de crear una tabla de contenido, se inserta el siguiente campo en el documento: **%{ TOC \\o \"1-3\" \\h \\z }**. Puedes copiar **%\\o \"1-3\" \\h \\z** y usarlo como parámetro de conmutadores.

Ten en cuenta que [InsertTableOfContents()](../) solo insertará un campo TOC, pero no construirá realmente la tabla de contenido. La tabla de contenido es generada por Microsoft Word cuando se actualiza el campo.

Si insertas una tabla de contenido usando este método y luego abres el archivo en Microsoft Word, no verás la tabla de contenido porque el campo TOC aún no se ha actualizado.

En Microsoft Word, los campos no se actualizan automáticamente al abrir un documento, pero puedes actualizar los campos en cualquier momento pulsando F9.

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

## Ver también

* Class [Field](../../../aspose.words.fields/field/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
