---
title: "Aspose::Words::Markup::StructuredDocumentTag::get_StyleName metodu"
linktitle: "get_StyleName"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Markup::StructuredDocumentTag::get_StyleName metodu. C++'da yapılandırılmış belge etiketine uygulanan stilin adını alır veya ayarlar."
type: docs
weight: 30000
url: /tr/cpp/aspose.words.markup/structureddocumenttag/get_stylename/
---
## StructuredDocumentTag::get_StyleName method


Yapılandırılmış belge etiketine uygulanan stilin adını alır veya ayarlar.

```cpp
System::String Aspose::Words::Markup::StructuredDocumentTag::get_StyleName()
```


## Örnekler



İçerik denetimi öğeleri için stillerle nasıl çalışılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Aşağıda bir belgeden yapılandırılmış belge etiketine stil uygulamanın iki yolu verilmiştir.
// 1 -  Belgenin stil koleksiyonundan bir stil nesnesi uygula:
System::SharedPtr<Aspose::Words::Style> quoteStyle = doc->get_Styles()->idx_get(Aspose::Words::StyleIdentifier::Quote);
auto sdtPlainText = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Inline);
sdtPlainText->set_Style(quoteStyle);

// 2 -  Belgedeki bir stili adını kullanarak referansla:
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

## Ayrıca Bakınız

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
