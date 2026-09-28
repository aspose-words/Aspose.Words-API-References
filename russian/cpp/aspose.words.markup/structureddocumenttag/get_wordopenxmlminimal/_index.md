---
title: "Aspose::Words::Markup::StructuredDocumentTag::get_WordOpenXMLMinimal method"
linktitle: "get_WordOpenXMLMinimal"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Markup::StructuredDocumentTag::get_WordOpenXMLMinimal метод. Возвращает строку, представляющую XML, содержащийся в узле в формате FlatOpc. В отличие от свойства WordOpenXML, этот метод генерирует упрощённый документ, исключающий любые части, не связанные с содержимым, в C++."
type: docs
weight: 33500
url: /ru/cpp/aspose.words.markup/structureddocumenttag/get_wordopenxmlminimal/
---
## StructuredDocumentTag::get_WordOpenXMLMinimal method


Возвращает строку, представляющую XML, содержащийся в узле в формате [FlatOpc](../../../aspose.words/saveformat/). В отличие от свойства [WordOpenXML](../get_wordopenxml/), этот метод генерирует упрощённый документ, исключающий любые части, не связанные с содержимым.

```cpp
System::String Aspose::Words::Markup::StructuredDocumentTag::get_WordOpenXMLMinimal()
```


## Примеры



Показывает, как работать со стилями для элементов управления содержимым.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ниже представлены два способа применения стиля из документа к structured document tag.
// 1 -  Применить объект стиля из коллекции стилей документа:
System::SharedPtr<Aspose::Words::Style> quoteStyle = doc->get_Styles()->idx_get(Aspose::Words::StyleIdentifier::Quote);
auto sdtPlainText = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Inline);
sdtPlainText->set_Style(quoteStyle);

// 2 -  Ссылка на стиль в документе по имени:
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

## См. также

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
