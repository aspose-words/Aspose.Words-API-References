---
title: "Aspose::Words::Markup::SdtType تعداد"
linktitle: "SdtType"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Markup::SdtType تعداد. يحدد نوع عقدة وسم المستند المنظم (SDT) في C++."
type: docs
weight: 21000
url: /ar/cpp/aspose.words.markup/sdttype/
---
## SdtType enum


يحدد نوع عقدة علامة المستند المهيكلة (SDT).

```cpp
enum class SdtType
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| None | 0 | لم يتم تعيين نوع للـ SDT. |
| المراجع | 1 | الـ SDT يمثل إدخالًا في الببليوغرافيا. |
| استشهاد | 2 | الـ SDT يمثل استشهادًا. |
| معادلة | 3 | الـ SDT يمثل معادلة. |
| قائمة منسدلة | 4 | يمثل الـ SDT قائمة منسدلة عند عرضها في المستند. |
| مربع تجميعي | 5 | يمثل الـ SDT مربع تجميعي عند عرضه في المستند. |
| التاريخ | 6 | يمثل الـ SDT أداة اختيار التاريخ عند عرضها في المستند. |
| BuildingBlockGallery | 7 | يمثل الـ SDT نوع معرض كتل البناء. |
| كائن جزء المستند | 8 | يمثل الـ SDT نوع جزء المستند. |
| مجموعة | 9 | يمثل الـ SDT تجميعًا مقيدًا عند عرضه في المستند. |
| صورة | 10 | يمثل الـ SDT صورة عند عرضها في المستند. |
| نص غني | 11 | يمثل الـ SDT مربع نص غني عند عرضه في المستند. |
| نص عادي | 12 | يمثل الـ SDT مربع نص عادي عند عرضه في المستند. |
| مربع اختيار | 13 | يمثل الـ SDT مربع اختيار عند عرضه في المستند. |
| قسم متكرر | 14 | يمثل الـ SDT نوع قسم متكرر عند عرضه في المستند. |
| عنصر قسم متكرر | 15 | يمثل الـ SDT عنصر قسم متكرر. |
| محدد الكيان | 16 | يمثل الـ SDT محدد كيان يتيح للمستخدم اختيار نسخة من نوع محتوى خارجي. |


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


يظهر كيفية ملء جدول بالبيانات من جزء XML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Markup::CustomXmlPart> xmlPart = doc->get_CustomXmlParts()->Add(u"Books", System::String(u"<books>") + u"<book>" + u"<title>Everyday Italian</title>" + u"<author>Giada De Laurentiis</author>" + u"</book>" + u"<book>" + u"<title>The C Programming Language</title>" + u"<author>Brian W. Kernighan, Dennis M. Ritchie</author>" + u"</book>" + u"<book>" + u"<title>Learning XML</title>" + u"<author>Erik T. Ray</author>" + u"</book>" + u"</books>");

// إنشاء رؤوس للبيانات من محتوى XML.
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Title");
builder->InsertCell();
builder->Write(u"Author");
builder->EndRow();
builder->EndTable();

// إنشاء جدول يحتوي على قسم متكرر داخله.
auto repeatingSectionSdt = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::RepeatingSection, Aspose::Words::Markup::MarkupLevel::Row);
repeatingSectionSdt->get_XmlMapping()->SetMapping(xmlPart, u"/books[1]/book", System::String::Empty);
table->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(repeatingSectionSdt);

// أضف عنصر قسم متكرر داخل القسم المتكرر وضع علامة عليه كصف.
// سيحتوي هذا الجدول على صف لكل عنصر يمكننا العثور عليه في مستند XML
// باستخدام مسار XPath "/books[1]/book"، والذي يوجد منه ثلاثة.
auto repeatingSectionItemSdt = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::RepeatingSectionItem, Aspose::Words::Markup::MarkupLevel::Row);
repeatingSectionSdt->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(repeatingSectionItemSdt);

auto row = System::MakeObject<Aspose::Words::Tables::Row>(doc);
repeatingSectionItemSdt->AppendChild<System::SharedPtr<Aspose::Words::Tables::Row>>(row);

// قم بربط بيانات XML بخلايا الجدول التي تم إنشاؤها للعنوان والمؤلف لكل كتاب.
auto titleSdt = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Cell);
titleSdt->get_XmlMapping()->SetMapping(xmlPart, u"/books[1]/book[1]/title[1]", System::String::Empty);
row->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(titleSdt);

auto authorSdt = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Cell);
authorSdt->get_XmlMapping()->SetMapping(xmlPart, u"/books[1]/book[1]/author[1]", System::String::Empty);
row->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(authorSdt);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.RepeatingSectionItem.docx");
```


يظهر كيفية إنشاء علامة مستند منسقة مجموعة على مستوى الصف.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();

// إنشاء علامة مستند منسقة مجموعة على مستوى الصف.
auto groupSdt = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::Group, Aspose::Words::Markup::MarkupLevel::Row);
table->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(groupSdt);
groupSdt->set_IsShowingPlaceholderText(false);
groupSdt->RemoveAllChildren();

// إنشاء صف فرعي لعلامة المستند المنسقة.
auto row = System::MakeObject<Aspose::Words::Tables::Row>(doc);
groupSdt->AppendChild<System::SharedPtr<Aspose::Words::Tables::Row>>(row);

auto cell = System::MakeObject<Aspose::Words::Tables::Cell>(doc);
row->AppendChild<System::SharedPtr<Aspose::Words::Tables::Cell>>(cell);

builder->EndTable();

// إدراج محتويات الخلية.
cell->EnsureMinimum();
builder->MoveTo(cell->get_LastParagraph());
builder->Write(u"Lorem ipsum dolor.");

// إدراج نص بعد الجدول.
builder->MoveTo(table->get_NextSibling());
builder->Write(u"Nulla blandit nisi.");

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.SdtAtRowLevel.docx");
```


يظهر كيفية إنشاء علامة مستند منسقة من نوع الاقتباس.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto sdt = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::Citation, Aspose::Words::Markup::MarkupLevel::Inline);
System::SharedPtr<Aspose::Words::Paragraph> paragraph = doc->get_FirstSection()->get_Body()->get_FirstParagraph();
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(sdt);

// إنشاء حقل اقتباس.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToParagraph(0, -1);
builder->InsertField(u"CITATION Ath22 \\l 1033 ", u"(John Lennon, 2022)");

// نقل الحقل إلى علامة المستند المنسقة.
while (sdt->get_NextSibling() != nullptr)
{
    sdt->AppendChild<System::SharedPtr<Aspose::Words::Node>>(sdt->get_NextSibling());
}

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.Citation.docx");
```

## انظر أيضًا

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
