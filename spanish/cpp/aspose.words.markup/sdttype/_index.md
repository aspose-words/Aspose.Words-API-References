---
title: "Aspose::Words::Markup::SdtType enumeración"
linktitle: "SdtType"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Enumeración Aspose::Words::Markup::SdtType. Especifica el tipo de un nodo de etiqueta de documento estructurado (SDT) en C++."
type: docs
weight: 21000
url: /es/cpp/aspose.words.markup/sdttype/
---
## SdtType enum


Especifica el tipo de un nodo de etiqueta de documento estructurado (SDT).

```cpp
enum class SdtType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | 0 | No se asigna ningún tipo al SDT. |
| Bibliografía | 1 | El SDT representa una entrada de bibliografía. |
| Citation | 2 | El SDT representa una cita. |
| Equation | 3 | El SDT representa una ecuación. |
| DropDownList | 4 | El SDT representa una lista desplegable cuando se muestra en el documento. |
| ComboBox | 5 | El SDT representa un cuadro combinado cuando se muestra en el documento. |
| Fecha | 6 | El SDT representa un selector de fecha cuando se muestra en el documento. |
| BuildingBlockGallery | 7 | El SDT representa un tipo de galería de bloques de construcción. |
| DocPartObj | 8 | El SDT representa un tipo de parte de documento. |
| Group | 9 | El SDT representa una agrupación restringida cuando se muestra en el documento. |
| Picture | 10 | El SDT representa una imagen cuando se muestra en el documento. |
| RichText | 11 | El SDT representa un cuadro de texto enriquecido cuando se muestra en el documento. |
| PlainText | 12 | El SDT representa un cuadro de texto plano cuando se muestra en el documento. |
| Checkbox | 13 | El SDT representa una casilla de verificación cuando se muestra en el documento. |
| RepeatingSection | 14 | El SDT representa un tipo de sección repetitiva cuando se muestra en el documento. |
| RepeatingSectionItem | 15 | El SDT representa un elemento de sección repetitiva. |
| EntityPicker | 16 | El SDT representa un selector de entidad que permite al usuario seleccionar una instancia de un tipo de contenido externo. |


## Ejemplos



Muestra cómo trabajar con estilos para elementos de control de contenido.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// A continuación se presentan dos formas de aplicar un estilo del documento a una etiqueta de documento estructurado.
// 1 -  Aplicar un objeto de estilo de la colección de estilos del documento:
System::SharedPtr<Aspose::Words::Style> quoteStyle = doc->get_Styles()->idx_get(Aspose::Words::StyleIdentifier::Quote);
auto sdtPlainText = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Inline);
sdtPlainText->set_Style(quoteStyle);

// 2 -  Referenciar un estilo en el documento por su nombre:
auto sdtRichText = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::RichText, Aspose::Words::Markup::MarkupLevel::Inline);
sdtRichText->set_StyleName(u"Quote");

builder->InsertNode(sdtPlainText);
builder->InsertNode(sdtRichText);

ASSERT_EQ(Aspose::Words::NodeType::StructuredDocumentTag, sdtPlainText->get_NodeType());

System::SharedPtr<Aspose::Words::NodeCollection> tags = doc->GetChildNodes(Aspose::Words::NodeType::StructuredDocumentTag, true);

for (auto&& node : System::IterateOver(tags))
{
    auto sdt = System::ExplicitCast<Aspose::Words::Markup::StructuredDocumentTag>(node);

    std::cout << sdt->get_WordOpenXMLMinimal() << std::endl;

    ASSERT_EQ(Aspose::Words::StyleIdentifier::Quote, sdt->get_Style()->get_StyleIdentifier());
    ASSERT_EQ(u"Quote", sdt->get_StyleName());
}
```


Muestra cómo rellenar una tabla con datos de una parte XML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Markup::CustomXmlPart> xmlPart = doc->get_CustomXmlParts()->Add(u"Books", System::String(u"<books>") + u"<book>" + u"<title>Everyday Italian</title>" + u"<author>Giada De Laurentiis</author>" + u"</book>" + u"<book>" + u"<title>The C Programming Language</title>" + u"<author>Brian W. Kernighan, Dennis M. Ritchie</author>" + u"</book>" + u"<book>" + u"<title>Learning XML</title>" + u"<author>Erik T. Ray</author>" + u"</book>" + u"</books>");

// Crea encabezados para los datos del contenido XML.
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Title");
builder->InsertCell();
builder->Write(u"Author");
builder->EndRow();
builder->EndTable();

// Crear una tabla con una sección repetitiva dentro.
auto repeatingSectionSdt = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::RepeatingSection, Aspose::Words::Markup::MarkupLevel::Row);
repeatingSectionSdt->get_XmlMapping()->SetMapping(xmlPart, u"/books[1]/book", System::String::Empty);
table->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(repeatingSectionSdt);

// Agregar un elemento de sección repetitiva dentro de la sección repetitiva y marcarlo como una fila.
// Esta tabla tendrá una fila para cada elemento que podamos encontrar en el documento XML
// usando la ruta XPath "/books[1]/book", de las cuales hay tres.
auto repeatingSectionItemSdt = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::RepeatingSectionItem, Aspose::Words::Markup::MarkupLevel::Row);
repeatingSectionSdt->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(repeatingSectionItemSdt);

auto row = System::MakeObject<Aspose::Words::Tables::Row>(doc);
repeatingSectionItemSdt->AppendChild<System::SharedPtr<Aspose::Words::Tables::Row>>(row);

// Mapear los datos XML con las celdas de tabla creadas para el título y el autor de cada libro.
auto titleSdt = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Cell);
titleSdt->get_XmlMapping()->SetMapping(xmlPart, u"/books[1]/book[1]/title[1]", System::String::Empty);
row->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(titleSdt);

auto authorSdt = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Cell);
authorSdt->get_XmlMapping()->SetMapping(xmlPart, u"/books[1]/book[1]/author[1]", System::String::Empty);
row->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(authorSdt);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.RepeatingSectionItem.docx");
```


Muestra cómo crear una etiqueta de documento estructurado de grupo a nivel de fila.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();

// Crear una etiqueta de documento estructurado de Grupo a nivel de fila.
auto groupSdt = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::Group, Aspose::Words::Markup::MarkupLevel::Row);
table->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(groupSdt);
groupSdt->set_IsShowingPlaceholderText(false);
groupSdt->RemoveAllChildren();

// Crear una fila hija de la etiqueta de documento estructurado.
auto row = System::MakeObject<Aspose::Words::Tables::Row>(doc);
groupSdt->AppendChild<System::SharedPtr<Aspose::Words::Tables::Row>>(row);

auto cell = System::MakeObject<Aspose::Words::Tables::Cell>(doc);
row->AppendChild<System::SharedPtr<Aspose::Words::Tables::Cell>>(cell);

builder->EndTable();

// Insertar contenido de la celda.
cell->EnsureMinimum();
builder->MoveTo(cell->get_LastParagraph());
builder->Write(u"Lorem ipsum dolor.");

// Insertar texto después de la tabla.
builder->MoveTo(table->get_NextSibling());
builder->Write(u"Nulla blandit nisi.");

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.SdtAtRowLevel.docx");
```


Muestra cómo crear una etiqueta de documento estructurado del tipo Cita.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto sdt = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::Citation, Aspose::Words::Markup::MarkupLevel::Inline);
System::SharedPtr<Aspose::Words::Paragraph> paragraph = doc->get_FirstSection()->get_Body()->get_FirstParagraph();
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(sdt);

// Crear un campo de Cita.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToParagraph(0, -1);
builder->InsertField(u"CITATION Ath22 \\l 1033 ", u"(John Lennon, 2022)");

// Mover el campo a la etiqueta de documento estructurado.
while (sdt->get_NextSibling() != nullptr)
{
    sdt->AppendChild<System::SharedPtr<Aspose::Words::Node>>(sdt->get_NextSibling());
}

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.Citation.docx");
```

## Ver también

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
