---
title: "Aspose::Words::DocumentBuilder::DocumentBuilder constructor"
linktitle: "DocumentBuilder"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::DocumentBuilder::DocumentBuilder constructor. Inicializa una nueva instancia de esta clase en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words/documentbuilder/documentbuilder/
---
## DocumentBuilder::DocumentBuilder() constructor


Inicializa una nueva instancia de esta clase.

```cpp
Aspose::Words::DocumentBuilder::DocumentBuilder()
```


## Ejemplos



Muestra cómo insertar texto con formato usando [DocumentBuilder](../).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Especifique el formato de fuente, luego agregue texto.
System::SharedPtr<Aspose::Words::Font> font = builder->get_Font();
font->set_Size(16);
font->set_Bold(true);
font->set_Color(System::Drawing::Color::get_Blue());
font->set_Name(u"Courier New");
font->set_Underline(Aspose::Words::Underline::Dash);

builder->Write(u"Hello world!");
```

## Ver también

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::DocumentBuilder(const System::SharedPtr\<Aspose::Words::Document\>\&) constructor


Inicializa una nueva instancia de esta clase.

```cpp
Aspose::Words::DocumentBuilder::DocumentBuilder(const System::SharedPtr<Aspose::Words::Document> &doc)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::Document\>\& | El objeto [Document](../../document/) al que adjuntar. |

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

* Class [Document](../../document/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::DocumentBuilder(const System::SharedPtr\<Aspose::Words::Document\>\&, const System::SharedPtr\<Aspose::Words::DocumentBuilderOptions\>\&) constructor


Inicializa una nueva instancia de esta clase.

```cpp
Aspose::Words::DocumentBuilder::DocumentBuilder(const System::SharedPtr<Aspose::Words::Document> &doc, const System::SharedPtr<Aspose::Words::DocumentBuilderOptions> &options)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::Document\>\& | El objeto [Document](../../document/) al que adjuntar. |
| opciones | const System::SharedPtr\<Aspose::Words::DocumentBuilderOptions\>\& | Opciones adicionales para el proceso de construcción del documento. |

## Ejemplos



Muestra cómo ignorar el formato de tabla para el contenido posterior.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builderOptions = System::MakeObject<Aspose::Words::DocumentBuilderOptions>();
builderOptions->set_ContextTableFormatting(true);
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc, builderOptions);

// Agrega contenido antes de la tabla.
// El tamaño de fuente predeterminado es 12.
builder->Writeln(u"Font size 12 here.");
builder->StartTable();
builder->InsertCell();
// Cambia el tamaño de fuente dentro de la tabla.
builder->get_Font()->set_Size(5);
builder->Write(u"Font size 5 here");
builder->InsertCell();
builder->Write(u"Font size 5 here");
builder->EndRow();
builder->EndTable();

// Si ContextTableFormatting es verdadero, entonces el formato de la tabla no se aplica al contenido posterior.
// Si ContextTableFormatting es falso, entonces el formato de la tabla se aplica al contenido posterior.
builder->Writeln(u"Font size 12 here.");

doc->Save(get_ArtifactsDir() + u"Table.ContextTableFormatting.docx");
```

## Ver también

* Class [Document](../../document/)
* Class [DocumentBuilderOptions](../../documentbuilderoptions/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::DocumentBuilder(const System::SharedPtr\<Aspose::Words::DocumentBuilderOptions\>\&) constructor


Inicializa una nueva instancia de esta clase.

```cpp
Aspose::Words::DocumentBuilder::DocumentBuilder(const System::SharedPtr<Aspose::Words::DocumentBuilderOptions> &options)
```


## Ejemplos



Muestra cómo ignorar el formato de tabla para el contenido posterior.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builderOptions = System::MakeObject<Aspose::Words::DocumentBuilderOptions>();
builderOptions->set_ContextTableFormatting(true);
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc, builderOptions);

// Agrega contenido antes de la tabla.
// El tamaño de fuente predeterminado es 12.
builder->Writeln(u"Font size 12 here.");
builder->StartTable();
builder->InsertCell();
// Cambia el tamaño de fuente dentro de la tabla.
builder->get_Font()->set_Size(5);
builder->Write(u"Font size 5 here");
builder->InsertCell();
builder->Write(u"Font size 5 here");
builder->EndRow();
builder->EndTable();

// Si ContextTableFormatting es verdadero, entonces el formato de la tabla no se aplica al contenido posterior.
// Si ContextTableFormatting es falso, entonces el formato de la tabla se aplica al contenido posterior.
builder->Writeln(u"Font size 12 here.");

doc->Save(get_ArtifactsDir() + u"Table.ContextTableFormatting.docx");
```

## Ver también

* Class [DocumentBuilderOptions](../../documentbuilderoptions/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
