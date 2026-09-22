---
title: "طريقة Aspose::Words::Markup::StructuredDocumentTag::get_StyleName"
linktitle: "get_StyleName"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Markup::StructuredDocumentTag::get_StyleName. يحصل على أو يحدد اسم النمط المطبق على الوسم المهيكل للوثيقة في C++."
type: docs
weight: 30000
url: /ar/cpp/aspose.words.markup/structureddocumenttag/get_stylename/
---
## StructuredDocumentTag::get_StyleName method


يحصل أو يعيّن اسم النمط المطبّق على علامة المستند المهيكلة.

```cpp
System::String Aspose::Words::Markup::StructuredDocumentTag::get_StyleName()
```


## أمثلة



يوضح كيفية العمل مع الأنماط لعناصر التحكم بالمحتوى.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// فيما يلي طريقتان لتطبيق نمط من المستند إلى StructuredDocumentTag.
// 1 -  تطبيق كائن نمط من مجموعة أنماط المستند:
System::SharedPtr<Aspose::Words::Style> quoteStyle = doc->get_Styles()->idx_get(Aspose::Words::StyleIdentifier::Quote);
auto sdtPlainText = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Inline);
sdtPlainText->set_Style(quoteStyle);

// 2 -  الإشارة إلى نمط في المستند بالاسم:
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

## انظر أيضًا

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
