---
title: "Aspose::Words::ParagraphFormat::get_Alignment método"
linktitle: "get_Alignment"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::ParagraphFormat::get_Alignment método. Obtiene o establece la alineación del texto para el párrafo en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words/paragraphformat/get_alignment/
---
## ParagraphFormat::get_Alignment method


Obtiene o establece la alineación del texto para el párrafo.

```cpp
Aspose::Words::ParagraphAlignment Aspose::Words::ParagraphFormat::get_Alignment()
```


## Ejemplos



Muestra cómo insertar un párrafo en el documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Font> font = builder->get_Font();
font->set_Size(16);
font->set_Bold(true);
font->set_Color(System::Drawing::Color::get_Blue());
font->set_Name(u"Arial");
font->set_Underline(Aspose::Words::Underline::Dash);

System::SharedPtr<Aspose::Words::ParagraphFormat> paragraphFormat = builder->get_ParagraphFormat();
paragraphFormat->set_FirstLineIndent(8);
paragraphFormat->set_Alignment(Aspose::Words::ParagraphAlignment::Justify);
paragraphFormat->set_AddSpaceBetweenFarEastAndAlpha(true);
paragraphFormat->set_AddSpaceBetweenFarEastAndDigit(true);
paragraphFormat->set_KeepTogether(true);

// El método "Writeln" finaliza el párrafo después de añadir texto
// y luego inicia una nueva línea, añadiendo un nuevo párrafo.
builder->Writeln(u"Hello world!");

ASSERT_TRUE(builder->get_CurrentParagraph()->get_IsEndOfDocument());
```


Muestra cómo construir un documento Aspose.Words manualmente.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Un documento en blanco contiene una sección, un cuerpo y un párrafo.
// Llame al método "RemoveAllChildren" para eliminar todos esos nodos,
// y termine con un nodo de documento sin hijos.
doc->RemoveAllChildren();

// Este documento ahora no tiene nodos hijos compuestos a los que podamos añadir contenido.
// Si deseamos editarlo, necesitaremos volver a poblar su colección de nodos.
// Primero, cree una nueva sección y luego añádala como hijo al nodo raíz del documento.
auto section = System::MakeObject<Aspose::Words::Section>(doc);
doc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(section);

// Establezca algunas propiedades de configuración de página para la sección.
section->get_PageSetup()->set_SectionStart(Aspose::Words::SectionStart::NewPage);
section->get_PageSetup()->set_PaperSize(Aspose::Words::PaperSize::Letter);

// Una sección necesita un cuerpo, que contendrá y mostrará todo su contenido
// en la página entre el encabezado y el pie de página de la sección.
auto body = System::MakeObject<Aspose::Words::Body>(doc);
section->AppendChild<System::SharedPtr<Aspose::Words::Body>>(body);

// Crea un párrafo, establece algunas propiedades de formato y luego añádelo como hijo al cuerpo.
auto para = System::MakeObject<Aspose::Words::Paragraph>(doc);

para->get_ParagraphFormat()->set_StyleName(u"Heading 1");
para->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);

body->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(para);

// Finalmente, agrega contenido al documento. Crea un run,
// establece su apariencia y contenido, y luego añádelo como hijo al párrafo.
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"Hello World!");
run->get_Font()->set_Color(System::Drawing::Color::get_Red());
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

ASSERT_EQ(u"Hello World!", doc->GetText().Trim());

doc->Save(get_ArtifactsDir() + u"Section.CreateManually.docx");
```

## Ver también

* Enum [ParagraphAlignment](../../paragraphalignment/)
* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
