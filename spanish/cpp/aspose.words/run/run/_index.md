---
title: "Constructor Aspose::Words::Run::Run"
linktitle: "Run"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Constructor Aspose::Words::Run::Run. Inicializa una nueva instancia de la clase Run en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words/run/run/
---
## Run::Run(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&) constructor


Inicializa una nueva instancia de la clase [Run](../).

```cpp
Aspose::Words::Run::Run(const System::SharedPtr<Aspose::Words::DocumentBase> &doc)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | El documento propietario. |
## Observaciones


Cuando se crea [Run](../), pertenece al documento especificado, pero aún no forma parte del documento y [ParentNode](../../node/get_parentnode/) es **null**.

Para agregar [Run](../) al documento, utilice [InsertAfter1()</see> o <see cref=\"Aspose::Words::CompositeNode::InsertBefore</tt>1(System::SharedPtr<<tt>0\\>, System::SharedPtr\\<Aspose::Words::Node\\>)\">InsertBefore1()](../) en el párrafo donde desea insertar el run.

## Ejemplos



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

* Class [DocumentBase](../../documentbase/)
* Class [Run](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Run::Run(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::String\&) constructor


Inicializa una nueva instancia de la clase **Run**.

```cpp
Aspose::Words::Run::Run(const System::SharedPtr<Aspose::Words::DocumentBase> &doc, const System::String &text)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | El documento propietario. |
| texto | const System::String\& | El texto del run. |
## Observaciones


Cuando se crea [Run](../), pertenece al documento especificado, pero aún no forma parte del documento y [ParentNode](../../node/get_parentnode/) es **null**.

Para agregar [Run](../) al documento, utilice [InsertAfter1()</see> o <see cref=\"Aspose::Words::CompositeNode::InsertBefore</tt>1(System::SharedPtr<<tt>0\\>, System::SharedPtr\\<Aspose::Words::Node\\>)\">InsertBefore1()](../) en el párrafo donde desea insertar el run.

## Ejemplos



Muestra cómo formatear una corrida de texto usando su propiedad de fuente.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!");

System::SharedPtr<Aspose::Words::Font> font = run->get_Font();
font->set_Name(u"Courier New");
font->set_Size(36);
font->set_HighlightColor(System::Drawing::Color::get_Yellow());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);
doc->Save(get_ArtifactsDir() + u"Font.CreateFormattedRun.docx");
```

## Ver también

* Class [DocumentBase](../../documentbase/)
* Class [Run](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
