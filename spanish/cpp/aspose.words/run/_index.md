---
title: "Clase Aspose::Words::Run"
linktitle: "Run"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::Run. Representa una ejecución de caracteres con el mismo formato de fuente. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 56000
url: /es/cpp/aspose.words/run/
---
## Run class


Representa una secuencia de caracteres con el mismo formato de fuente. Para obtener más información, visite el artículo de documentación [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
class Run : public Aspose::Words::Inline
```

## Métodos

| Método | Descripción |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Acepta un visitante. |
| [Clone](../node/clone/)(bool) | Crea un duplicado del nodo. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Especifica un identificador de nodo personalizado. |
| virtual [get_Document](../node/get_document/)() const | Obtiene el documento al que pertenece este nodo. |
| [get_Font](../inline/get_font/)() | Proporciona acceso al formato de fuente de este objeto. |
| virtual [get_IsComposite](../node/get_iscomposite/)() | Devuelve **true** si este nodo puede contener otros nodos. |
| [get_IsDeleteRevision](../inline/get_isdeleterevision/)() | Devuelve true si este objeto fue eliminado en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [get_IsFormatRevision](../inline/get_isformatrevision/)() | Devuelve true si el formato del objeto se modificó en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [get_IsInsertRevision](../inline/get_isinsertrevision/)() | Devuelve true si este objeto fue insertado en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [get_IsMoveFromRevision](../inline/get_ismovefromrevision/)() | Devuelve **true** si este objeto fue movido (eliminado) en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [get_IsMoveToRevision](../inline/get_ismovetorevision/)() | Devuelve **true** si este objeto fue movido (insertado) en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [get_IsPhoneticGuide](./get_isphoneticguide/)() | Obtiene un valor booleano que indica si la ejecución es una guía fonética. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | Obtiene el nodo que sigue inmediatamente a este nodo. |
| [get_NodeType](./get_nodetype/)() const override | Devuelve [Run](../nodetype/). |
| [get_ParentNode](../node/get_parentnode/)() | Obtiene el padre inmediato de este nodo. |
| [get_ParentParagraph](../inline/get_parentparagraph/)() | Recupera el [Paragraph](../paragraph/) padre de este nodo. |
| [get_PhoneticGuide](./get_phoneticguide/)() | Obtiene un objeto [PhoneticGuide](./get_phoneticguide/). |
| [get_PreviousSibling](../node/get_previoussibling/)() | Obtiene el nodo que precede inmediatamente a este nodo. |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_Range](../node/get_range/)() | Devuelve un objeto [Range](../range/) que representa la porción de un documento que está contenida en este nodo. |
| [get_Text](./get_text/)() const | Obtiene o establece el texto de la ejecución. |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | Obtiene el primer ancestro del [NodeType](../nodetype/) especificado. |
| [GetAncestorOf](../node/getancestorof/)() |  |
| [GetText](./gettext/)() override | Obtiene el texto de la ejecución. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Obtiene el nodo siguiente según el algoritmo de recorrido en preorden del árbol. |
| static [NodeTypeToString](../node/nodetypetostring/)(Aspose::Words::NodeType) | Un método de utilidad que convierte un valor de enumeración de tipo de nodo en una cadena legible para el usuario. |
| [PreviousPreOrder](../node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Obtiene el nodo anterior según el algoritmo de recorrido en preorden del árbol. |
| [Remove](../node/remove/)() | Se elimina a sí mismo del nodo padre. |
| [Run](./run/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&) | Inicializa una nueva instancia de la clase [Run](./). |
| [Run](./run/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::String\&) | Inicializa una nueva instancia de la clase **Run**. |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | Método setter para [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/). |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_Text](./set_text/)(const System::String\&) | Método setter para [Aspose::Words::Run::get_Text](./get_text/). |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | Exporta el contenido del nodo a una cadena en el formato especificado. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exporta el contenido del nodo a una cadena usando las opciones de guardado especificadas. |
| static [Type](./type/)() |  |
## Observaciones


Todo el texto del documento se almacena en corridas de texto.

[Run](./) can only be a child of [Paragraph](../paragraph/) or inline [StructuredDocumentTag](../../aspose.words.markup/structureddocumenttag/).

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


Muestra cómo agregar, actualizar y eliminar nodos hijos en la colección de hijos de un [CompositeNode](../compositenode/).
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

* Class [Inline](../inline/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
