---
title: "Aspose::Words::Range::Replace método"
linktitle: "Replace"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Range::Replace método. Reemplaza todas las apariciones de un patrón de caracteres especificado por una expresión regular con otra cadena en C++."
type: docs
weight: 12000
url: /es/cpp/aspose.words/range/replace/
---
## Range::Replace(const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) method


Reemplaza todas las apariciones de un patrón de caracteres especificado por una expresión regular con otra cadena.

```cpp
int32_t Aspose::Words::Range::Replace(const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| patrón | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Un patrón de expresión regular utilizado para encontrar coincidencias. |
| reemplazo | const System::String\& | Una cadena para reemplazar todas las apariciones del patrón. |

### ReturnValue

El número de reemplazos realizados.
## Observaciones


Reemplaza toda la coincidencia capturada por la expresión regular.

El método puede procesar saltos en ambas cadenas de patrón y de reemplazo.

Debe usar metacaracteres especiales si necesita trabajar con saltos:

* **%&p** - paragraph break
* **%&b** - section break
* **%&m** - page break
* **%&l** - manual line break



## Ejemplos



Muestra cómo reemplazar todas las ocurrencias de un patrón de expresión regular con otro texto.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"I decided to get the curtains in gray, ideal for the grey-accented room.");

doc->get_Range()->Replace(System::MakeObject<System::Text::RegularExpressions::Regex>(u"gr(a|e)y"), u"lavender");

ASSERT_EQ(u"I decided to get the curtains in lavender, ideal for the lavender-accented room.", doc->GetText().Trim());
```

## Ver también

* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Range::Replace(const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Reemplaza todas las apariciones de un patrón de caracteres especificado por una expresión regular con otra cadena.

```cpp
int32_t Aspose::Words::Range::Replace(const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| patrón | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Un patrón de expresión regular utilizado para encontrar coincidencias. |
| reemplazo | const System::String\& | Una cadena para reemplazar todas las apariciones del patrón. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) objeto para especificar opciones adicionales. |

### ReturnValue

El número de reemplazos realizados.
## Observaciones


Reemplaza toda la coincidencia capturada por la expresión regular.

El método puede procesar saltos en ambas cadenas de patrón y de reemplazo.

Debe usar metacaracteres especiales si necesita trabajar con saltos:

* **%&p** - paragraph break
* **%&b** - section break
* **%&m** - page break
* **%&l** - manual line break
* **%&&** - & character



## Ver también

* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Range::Replace(const System::String\&, const System::String\&) method


Reemplaza todas las apariciones de un patrón de cadena de caracteres especificado con una cadena de reemplazo.

```cpp
int32_t Aspose::Words::Range::Replace(const System::String &pattern, const System::String &replacement)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| patrón | const System::String\& | Una cadena a ser reemplazada. |
| reemplazo | const System::String\& | Una cadena para reemplazar todas las apariciones del patrón. |

### ReturnValue

El número de reemplazos realizados.
## Observaciones


El patrón no se usará como expresión regular. Por favor use [Replace()](../) si necesita expresiones regulares.

Se utilizó comparación sin distinción entre mayúsculas y minúsculas.

El método puede procesar saltos en ambas cadenas de patrón y de reemplazo.

Debe usar metacaracteres especiales si necesita trabajar con saltos:

* **%&p** - paragraph break
* **%&b** - section break
* **%&m** - page break
* **%&l** - manual line break



## Ejemplos



Muestra cómo realizar una operación de buscar y reemplazar texto en el contenido de un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Greetings, _FullName_!");

// Realice una operación de buscar y reemplazar en el contenido de nuestro documento y verifique la cantidad de reemplazos que se realizaron.
int32_t replacementCount = doc->get_Range()->Replace(u"_FullName_", u"John Doe");

ASSERT_EQ(1, replacementCount);
ASSERT_EQ(u"Greetings, John Doe!", doc->GetText().Trim());
```


Muestra cómo agregar formato a los párrafos en los que una operación de buscar y reemplazar ha encontrado coincidencias.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Every paragraph that ends with a full stop like this one will be right aligned.");
builder->Writeln(u"This one will not!");
builder->Write(u"This one also will.");

System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

ASSERT_EQ(Aspose::Words::ParagraphAlignment::Left, paragraphs->idx_get(0)->get_ParagraphFormat()->get_Alignment());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Left, paragraphs->idx_get(1)->get_ParagraphFormat()->get_Alignment());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Left, paragraphs->idx_get(2)->get_ParagraphFormat()->get_Alignment());

// Podemos usar un objeto "FindReplaceOptions" para modificar el proceso de buscar y reemplazar.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Establezca la propiedad "Alignment" a "ParagraphAlignment.Right" para alinear a la derecha cada párrafo
// que contiene una coincidencia que la operación de buscar y reemplazar encuentra.
options->get_ApplyParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Right);

// Reemplace cada punto que está justo antes de un salto de párrafo con un signo de exclamación.
int32_t count = doc->get_Range()->Replace(u".&p", u"!&p", options);

ASSERT_EQ(2, count);
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Right, paragraphs->idx_get(0)->get_ParagraphFormat()->get_Alignment());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Left, paragraphs->idx_get(1)->get_ParagraphFormat()->get_Alignment());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Right, paragraphs->idx_get(2)->get_ParagraphFormat()->get_Alignment());
ASSERT_EQ(System::String(u"Every paragraph that ends with a full stop like this one will be right aligned!\r") + u"This one will not!\r" + u"This one also will!", doc->GetText().Trim());
```

## Ver también

* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Range::Replace(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Reemplaza todas las apariciones de un patrón de cadena de caracteres especificado con una cadena de reemplazo.

```cpp
int32_t Aspose::Words::Range::Replace(const System::String &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| patrón | const System::String\& | Una cadena a ser reemplazada. |
| reemplazo | const System::String\& | Una cadena para reemplazar todas las apariciones del patrón. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) objeto para especificar opciones adicionales. |

### ReturnValue

El número de reemplazos realizados.
## Observaciones


El patrón no se usará como expresión regular. Por favor use [Replace()](../) si necesita expresiones regulares.

El método puede procesar saltos en ambas cadenas de patrón y de reemplazo.

Debe usar metacaracteres especiales si necesita trabajar con saltos:

* **%&p** - paragraph break
* **%&b** - section break
* **%&m** - page break
* **%&l** - manual line break
* **%&&** - & character



## Ejemplos



Muestra cómo reemplazar texto en el pie de página de un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footer.docx");

System::SharedPtr<Aspose::Words::HeaderFooterCollection> headersFooters = doc->get_FirstSection()->get_HeadersFooters();
System::SharedPtr<Aspose::Words::HeaderFooter> footer = headersFooters->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary);

auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
options->set_MatchCase(false);
options->set_FindWholeWordsOnly(false);

int32_t currentYear = System::DateTime::get_Now().get_Year();
footer->get_Range()->Replace(u"(C) 2006 Aspose Pty Ltd.", System::String::Format(u"Copyright (C) {0} by Aspose Pty Ltd.", currentYear), options);

doc->Save(get_ArtifactsDir() + u"HeaderFooter.ReplaceText.docx");
```


Muestra cómo alternar la sensibilidad a mayúsculas y minúsculas al realizar una operación de buscar y reemplazar.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Ruby bought a ruby necklace.");

// Podemos usar un objeto "FindReplaceOptions" para modificar el proceso de buscar y reemplazar.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Establezca la bandera "MatchCase" a "true" para aplicar sensibilidad a mayúsculas y minúsculas al buscar cadenas para reemplazar.
// Establezca la bandera "MatchCase" a "false" para ignorar mayúsculas y minúsculas al buscar texto para reemplazar.
options->set_MatchCase(matchCase);

doc->get_Range()->Replace(u"Ruby", u"Jade", options);

ASSERT_EQ(matchCase ? System::String(u"Jade bought a ruby necklace.") : System::String(u"Jade bought a Jade necklace."), doc->GetText().Trim());
```


Muestra cómo alternar operaciones de buscar y reemplazar que solo afectan palabras independientes.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Jackson will meet you in Jacksonville.");

// Podemos usar un objeto "FindReplaceOptions" para modificar el proceso de buscar y reemplazar.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Establezca la bandera "FindWholeWordsOnly" a "true" para reemplazar el texto encontrado si no forma parte de otra palabra.
// Establezca la bandera "FindWholeWordsOnly" a "false" para reemplazar todo el texto sin importar su contexto.
options->set_FindWholeWordsOnly(findWholeWordsOnly);

doc->get_Range()->Replace(u"Jackson", u"Louis", options);

ASSERT_EQ(findWholeWordsOnly ? System::String(u"Louis will meet you in Jacksonville.") : System::String(u"Louis will meet you in Louisville."), doc->GetText().Trim());
```


Muestra cómo reemplazar todas las instancias de una cadena de texto en una tabla y celda.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Carrots");
builder->InsertCell();
builder->Write(u"50");
builder->EndRow();
builder->InsertCell();
builder->Write(u"Potatoes");
builder->InsertCell();
builder->Write(u"50");
builder->EndTable();

auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
options->set_MatchCase(true);
options->set_FindWholeWordsOnly(true);

// Realice una operación de buscar y reemplazar en una tabla completa.
table->get_Range()->Replace(u"Carrots", u"Eggs", options);

// Realice una operación de buscar y reemplazar en la última celda de la última fila de la tabla.
table->get_LastRow()->get_LastCell()->get_Range()->Replace(u"50", u"20", options);

ASSERT_EQ(System::String(u"Eggs\a50\a\a") + u"Potatoes\a20\a\a", table->GetText().Trim());
```

## Ver también

* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
