---
title: "Aspose::Words::DocumentBuilder::InsertHtml método"
linktitle: "InsertHtml"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::DocumentBuilder::InsertHtml método. Inserta una cadena HTML en el documento en C++."
type: docs
weight: 37000
url: /es/cpp/aspose.words/documentbuilder/inserthtml/
---
## DocumentBuilder::InsertHtml(const System::String\&) method


Inserta una cadena HTML en el documento.

```cpp
void Aspose::Words::DocumentBuilder::InsertHtml(const System::String &html)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| html | const System::String\& | Una cadena HTML para insertar en el documento. |

## Ejemplos



Muestra cómo usar un document builder para insertar contenido html en un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

const System::String html = System::String(u"<p align='right'>Paragraph right</p>") + u"<b>Implicit paragraph left</b>" + u"<div align='center'>Div center</div>" + u"<h1 align='left'>Heading 1 left.</h1>";

builder->InsertHtml(html);

// Insertar código HTML analiza el formato de cada elemento y lo convierte en un formato de texto de documento equivalente.
System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

ASSERT_EQ(u"Paragraph right", paragraphs->idx_get(0)->GetText().Trim());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Right, paragraphs->idx_get(0)->get_ParagraphFormat()->get_Alignment());

ASSERT_EQ(u"Implicit paragraph left", paragraphs->idx_get(1)->GetText().Trim());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Left, paragraphs->idx_get(1)->get_ParagraphFormat()->get_Alignment());
ASSERT_TRUE(paragraphs->idx_get(1)->get_Runs()->idx_get(0)->get_Font()->get_Bold());

ASSERT_EQ(u"Div center", paragraphs->idx_get(2)->GetText().Trim());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Center, paragraphs->idx_get(2)->get_ParagraphFormat()->get_Alignment());

ASSERT_EQ(u"Heading 1 left.", paragraphs->idx_get(3)->GetText().Trim());
ASSERT_EQ(u"Heading 1", paragraphs->idx_get(3)->get_ParagraphFormat()->get_Style()->get_Name());

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertHtml.docx");
```

## Ver también

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertHtml(const System::String\&, Aspose::Words::HtmlInsertOptions) method


Inserta una cadena HTML en el documento. Permite especificar opciones adicionales.

```cpp
void Aspose::Words::DocumentBuilder::InsertHtml(const System::String &html, Aspose::Words::HtmlInsertOptions options)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| html | const System::String\& | Una cadena HTML para insertar en el documento. |
| opciones | Aspose::Words::HtmlInsertOptions | Opciones que se utilizan cuando se inserta una cadena HTML. |

## Ver también

* Enum [HtmlInsertOptions](../../htmlinsertoptions/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertHtml(const System::String\&, bool) method


Inserta una cadena HTML en el documento.

```cpp
void Aspose::Words::DocumentBuilder::InsertHtml(const System::String &html, bool useBuilderFormatting)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| html | const System::String\& | Una cadena HTML para insertar en el documento. |
| useBuilderFormatting | bool | Un valor que indica si el formato especificado en [DocumentBuilder](../) se usa como formato base para el texto importado desde HTML. |
## Observaciones


Puede usar este método para insertar un fragmento HTML o un documento HTML completo.

Cuando *useBuilderFormatting* es **false**, el formato de [DocumentBuilder](../) se ignora y el formato del texto insertado se basa en el formato HTML predeterminado. Como resultado, el texto se ve como se renderiza en los navegadores.

Cuando *useBuilderFormatting* es **true**, el formato del texto insertado se basa en el formato de [DocumentBuilder](../), y el texto se ve como si se hubiera insertado con [Write()](../).

## Ejemplos



Muestra cómo aplicar el formato de un document builder al insertar contenido HTML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Establezca una alineación de texto para el builder, inserte un párrafo HTML con una alineación especificada y otro sin ella.
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Distributed);
builder->InsertHtml(System::String(u"<p align='right'>Paragraph 1.</p>") + u"<p>Paragraph 2.</p>", useBuilderFormatting);

System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

// El primer párrafo tiene una alineación especificada. Cuando InsertHtml analiza el código HTML,
// el valor de alineación del párrafo encontrado en el código HTML siempre sobrescribe el valor del document builder.
ASSERT_EQ(u"Paragraph 1.", paragraphs->idx_get(0)->GetText().Trim());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Right, paragraphs->idx_get(0)->get_ParagraphFormat()->get_Alignment());

// El segundo párrafo no tiene alineación especificada. Puede que su valor de alineación se rellene
// por el valor del builder dependiendo de la bandera que pasamos al método InsertHtml.
ASSERT_EQ(u"Paragraph 2.", paragraphs->idx_get(1)->GetText().Trim());
ASSERT_EQ(useBuilderFormatting ? Aspose::Words::ParagraphAlignment::Distributed : Aspose::Words::ParagraphAlignment::Left, paragraphs->idx_get(1)->get_ParagraphFormat()->get_Alignment());

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertHtmlWithFormatting.docx");
```

## Ver también

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
