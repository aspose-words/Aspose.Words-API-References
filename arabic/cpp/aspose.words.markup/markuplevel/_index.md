---
title: "Aspose::Words::Markup::MarkupLevel تعداد"
linktitle: "MarkupLevel"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Markup::MarkupLevel enum. يحدد المستوى في شجرة المستند حيث يمكن أن يحدث StructuredDocumentTag معين في C++."
type: docs
weight: 17000
url: /ar/cpp/aspose.words.markup/markuplevel/
---
## MarkupLevel enum


يحدد المستوى في شجرة المستند حيث يمكن أن يحدث [StructuredDocumentTag](../structureddocumenttag/) معين.

```cpp
enum class MarkupLevel
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| غير معروف | 0 | يحدد القيمة غير المعروفة أو غير الصالحة. |
| متضمن | 1 | العنصر يحدث على المستوى المضمن (مثال: بين مقاطع النص). |
| Block | 2 | العنصر يحدث على مستوى الكتلة (مثال: بين الجداول والفقرات). |
| Row | 3 | العنصر يحدث بين الصفوف في جدول. |
| خلية | 4 | العنصر يحدث بين الخلايا في صف. |


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

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
