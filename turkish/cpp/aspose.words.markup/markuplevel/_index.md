---
title: "Aspose::Words::Markup::MarkupLevel enum"
linktitle: "MarkupLevel"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Markup::MarkupLevel enum. Belirli bir StructuredDocumentTag'in C++'da belge ağacında ortaya çıkabileceği seviyeyi belirtir."
type: docs
weight: 17000
url: /tr/cpp/aspose.words.markup/markuplevel/
---
## MarkupLevel enum


Belirli bir [StructuredDocumentTag](../structureddocumenttag/) öğesinin belge ağacında ortaya çıkabileceği seviyeyi belirtir.

```cpp
enum class MarkupLevel
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| Bilinmiyor | 0 | Bilinmeyen veya geçersiz değeri belirtir. |
| Satır içi | 1 | Öğe satır içi seviyesinde (ör. metin akışları arasında) ortaya çıkar. |
| Block | 2 | Öğe blok seviyesinde (ör. tablolar ve paragraflar arasında) ortaya çıkar. |
| Row | 3 | Öğe bir tabloda satırlar arasında ortaya çıkar. |
| Hücre | 4 | Öğe bir satırda hücreler arasında ortaya çıkar. |


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

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
