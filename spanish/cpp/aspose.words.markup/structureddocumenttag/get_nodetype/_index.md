---
title: "Aspose::Words::Markup::StructuredDocumentTag::get_NodeType método"
linktitle: "get_NodeType"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Markup::StructuredDocumentTag::get_NodeType método. Devuelve StructuredDocumentTag en C++."
type: docs
weight: 25000
url: /es/cpp/aspose.words.markup/structureddocumenttag/get_nodetype/
---
## StructuredDocumentTag::get_NodeType method


Devuelve [StructuredDocumentTag](../../../aspose.words/nodetype/).

```cpp
Aspose::Words::NodeType Aspose::Words::Markup::StructuredDocumentTag::get_NodeType() const override
```


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

## Ver también

* Enum [NodeType](../../../aspose.words/nodetype/)
* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
