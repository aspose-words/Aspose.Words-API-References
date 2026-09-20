---
title: "Aspose::Words::Paragraph::GetText método"
linktitle: "GetText"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Paragraph::GetText. Obtiene el texto de este párrafo incluyendo el carácter de fin de párrafo en C++."
type: docs
weight: 27000
url: /es/cpp/aspose.words/paragraph/gettext/
---
## Paragraph::GetText method


Obtiene el texto de este párrafo incluyendo el carácter de fin de párrafo.

```cpp
System::String Aspose::Words::Paragraph::GetText() override
```

## Observaciones


El texto de todos los nodos hijos se concatena y se agrega el carácter de fin de párrafo de la siguiente manera:

* If the paragraph is the last paragraph of [Body](../../body/), then [SectionBreak](../../controlchar/sectionbreak/) (\x000c) is appended.
* If the paragraph is the last paragraph of [Cell](../../../aspose.words.tables/cell/), then [Cell](../../controlchar/cell/) (\x0007) is appended.
* For all other paragraphs [ParagraphBreak](../../controlchar/paragraphbreak/) (\r) is appended.



La cadena devuelta incluye todos los caracteres de control y especiales como se describe en [ControlChar](../../controlchar/).

## Ejemplos



Muestra cómo agregar, actualizar y eliminar nodos hijos en la colección de hijos de un [CompositeNode](../../compositenode/).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Un documento vacío, por defecto, tiene un párrafo.
ASSERT_EQ(1, doc->get_FirstSection()->get_Body()->get_Paragraphs()->get_Count());

// Los nodos compuestos, como nuestro párrafo, pueden contener otros nodos compuestos e inline como hijos.
System::SharedPtr<Aspose::Words::Paragraph> paragraph = doc->get_FirstSection()->get_Body()->get_FirstParagraph();
auto paragraphText = System::MakeObject<Aspose::Words::Run>(doc, u"Initial text. ");
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(paragraphText);

// Crea tres nodos de run más.
auto run1 = System::MakeObject<Aspose::Words::Run>(doc, u"Run 1. ");
auto run2 = System::MakeObject<Aspose::Words::Run>(doc, u"Run 2. ");
auto run3 = System::MakeObject<Aspose::Words::Run>(doc, u"Run 3. ");

// El cuerpo del documento no mostrará estas corridas hasta que las insertemos en un nodo compuesto
// que a su vez es parte del árbol de nodos del documento, como hicimos con la primera corrida.
// Podemos determinar dónde aparecen los contenidos de texto de los nodos que insertamos
// aparece en el documento especificando una ubicación de inserción relativa a otro nodo en el párrafo.
ASSERT_EQ(u"Initial text.", paragraph->GetText().Trim());

// Inserta la segunda corrida en el párrafo delante de la corrida inicial.
paragraph->InsertBefore<System::SharedPtr<Aspose::Words::Run>>(run2, paragraphText);

ASSERT_EQ(u"Run 2. Initial text.", paragraph->GetText().Trim());

// Inserta la tercera corrida después de la corrida inicial.
paragraph->InsertAfter<System::SharedPtr<Aspose::Words::Run>>(run3, paragraphText);

ASSERT_EQ(u"Run 2. Initial text. Run 3.", paragraph->GetText().Trim());

// Inserta la primera corrida al inicio de la colección de nodos hijos del párrafo.
paragraph->PrependChild<System::SharedPtr<Aspose::Words::Run>>(run1);

ASSERT_EQ(u"Run 1. Run 2. Initial text. Run 3.", paragraph->GetText().Trim());
ASSERT_EQ(4, paragraph->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// Podemos modificar el contenido de la corrida editando y eliminando los nodos hijos existentes.
(System::ExplicitCast<Aspose::Words::Run>(paragraph->GetChildNodes(Aspose::Words::NodeType::Run, true)->idx_get(1)))->set_Text(u"Updated run 2. ");
paragraph->GetChildNodes(Aspose::Words::NodeType::Run, true)->Remove(paragraphText);

ASSERT_EQ(u"Run 1. Updated run 2. Run 3.", paragraph->GetText().Trim());
ASSERT_EQ(3, paragraph->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());
```

## Ver también

* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
