---
title: "Aspose::Words::Fields::FieldRD::get_FileName método"
linktitle: "get_FileName"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fields::FieldRD::get_FileName método. Obtiene o establece el nombre del archivo a incluir al generar una tabla de contenido, tabla de autoridades o índice en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.fields/fieldrd/get_filename/
---
## FieldRD::get_FileName method


Obtiene o establece el nombre del archivo que se incluirá al generar una tabla de contenido, tabla de autoridades o índice.

```cpp
System::String Aspose::Words::Fields::FieldRD::get_FileName()
```


## Ejemplos



Muestra cómo usar el campo RD para crear entradas de tabla de contenido a partir de encabezados en otros documentos.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Utilice un constructor de documentos para insertar una tabla de contenido,
// y luego agregue una entrada para la tabla de contenido en la página siguiente.
builder->InsertField(Aspose::Words::Fields::FieldType::FieldTOC, true);
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->get_CurrentParagraph()->get_ParagraphFormat()->set_StyleName(u"Heading 1");
builder->Writeln(u"TOC entry from within this document");

// Inserte un campo RD, que hace referencia a otro documento del sistema de archivos local en su propiedad FileName.
// La tabla de contenido ahora también aceptará todos los encabezados del documento referenciado como entradas para su tabla.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldRD>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldRefDoc, true));
field->set_FileName(get_ArtifactsDir() + u"ReferencedDocument.docx");

ASSERT_EQ(System::String::Format(u" RD  {0}ReferencedDocument.docx", get_ArtifactsDir().Replace(u"\\", u"\\\\")), field->GetFieldCode());

// Cree el documento al que el campo RD está haciendo referencia e inserte un encabezado.
// Este encabezado aparecerá como una entrada en el campo TOC de nuestro primer documento.
auto referencedDoc = System::MakeObject<Aspose::Words::Document>();
auto refDocBuilder = System::MakeObject<Aspose::Words::DocumentBuilder>(referencedDoc);
refDocBuilder->get_CurrentParagraph()->get_ParagraphFormat()->set_StyleName(u"Heading 1");
refDocBuilder->Writeln(u"TOC entry from referenced document");
referencedDoc->Save(get_ArtifactsDir() + u"ReferencedDocument.docx");

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.RD.docx");
```

## Ver también

* Class [FieldRD](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
