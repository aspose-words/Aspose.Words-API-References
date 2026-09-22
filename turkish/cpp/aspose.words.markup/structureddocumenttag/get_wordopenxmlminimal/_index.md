---
title: "Aspose::Words::Markup::StructuredDocumentTag::get_WordOpenXMLMinimal yöntemi"
linktitle: "get_WordOpenXMLMinimal"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Markup::StructuredDocumentTag::get_WordOpenXMLMinimal yöntemi. Düğüm içinde bulunan XML'i FlatOpc biçiminde temsil eden bir dize alır. WordOpenXML özelliğinin aksine, bu yöntem C++'ta içerik dışı bölümleri hariç tutan sadeleştirilmiş bir belge oluşturur."
type: docs
weight: 33500
url: /tr/cpp/aspose.words.markup/structureddocumenttag/get_wordopenxmlminimal/
---
## StructuredDocumentTag::get_WordOpenXMLMinimal method


Düğüm içinde bulunan XML'i [FlatOpc](../../../aspose.words/saveformat/) biçiminde temsil eden bir dize alır. [WordOpenXML](../get_wordopenxml/) özelliğinin aksine, bu yöntem içerik dışı bölümleri hariç tutan sadeleştirilmiş bir belge oluşturur.

```cpp
System::String Aspose::Words::Markup::StructuredDocumentTag::get_WordOpenXMLMinimal()
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
