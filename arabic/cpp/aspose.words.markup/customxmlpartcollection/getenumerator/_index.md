---
title: "طريقة Aspose::Words::Markup::CustomXmlPartCollection::GetEnumerator"
linktitle: "GetEnumerator"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Markup::CustomXmlPartCollection::GetEnumerator. يرجع كائن تعداد يمكن استخدامه للتنقل عبر جميع العناصر في المجموعة في C++."
type: docs
weight: 12000
url: /ar/cpp/aspose.words.markup/customxmlpartcollection/getenumerator/
---
## CustomXmlPartCollection::GetEnumerator method


يرجع كائن عداد يمكن استخدامه للتنقل عبر جميع العناصر في المجموعة.

```cpp
System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Markup::CustomXmlPart>>> Aspose::Words::Markup::CustomXmlPartCollection::GetEnumerator() override
```


## أمثلة



يوضح كيفية إنشاء علامة مستند منسقة مع بيانات XML مخصصة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// أنشئ جزء XML يحتوي على بيانات وأضفه إلى مجموعة المستند.
// إذا قمنا بتمكين علامة التبويب "Developer" في Microsoft Word،
// يمكننا العثور على العناصر من هذه المجموعة في "XML Mapping Pane"، إلى جانب بعض العناصر الافتراضية.
System::String xmlPartId = System::Guid::NewGuid().ToString(u"B");
System::String xmlPartContent = u"<root><text>Hello world!</text></root>";
System::SharedPtr<Aspose::Words::Markup::CustomXmlPart> xmlPart = doc->get_CustomXmlParts()->Add(xmlPartId, xmlPartContent);

ASPOSE_ASSERT_EQ(System::Text::Encoding::get_ASCII()->GetBytes(xmlPartContent), xmlPart->get_Data());
ASSERT_EQ(xmlPartId, xmlPart->get_Id());

// فيما يلي طريقتان للإشارة إلى أجزاء XML.
// 1 -  عبر فهرس في مجموعة أجزاء XML المخصصة:
ASPOSE_ASSERT_EQ(xmlPart, doc->get_CustomXmlParts()->idx_get(0));

// 2 -  عبر GUID:
ASPOSE_ASSERT_EQ(xmlPart, doc->get_CustomXmlParts()->GetById(xmlPartId));

// أضف ارتباط مخطط XML.
xmlPart->get_Schemas()->Add(u"http://www.w3.org/2001/XMLSchema");

// استنسخ جزءًا، ثم أدخله في المجموعة.
System::SharedPtr<Aspose::Words::Markup::CustomXmlPart> xmlPartClone = xmlPart->Clone();
xmlPartClone->set_Id(System::Guid::NewGuid().ToString(u"B"));
doc->get_CustomXmlParts()->Add(xmlPartClone);

ASSERT_EQ(2, doc->get_CustomXmlParts()->get_Count());

// تجول عبر المجموعة واطبع محتويات كل جزء.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Markup::CustomXmlPart>>> enumerator = doc->get_CustomXmlParts()->GetEnumerator();
    int32_t index = 0;
    while (enumerator->MoveNext())
    {
        std::cout << System::String::Format(u"XML part index {0}, ID: {1}", index, enumerator->get_Current()->get_Id()) << std::endl;
        std::cout << System::String::Format(u"\tContent: {0}", System::Text::Encoding::get_UTF8()->GetString(enumerator->get_Current()->get_Data())) << std::endl;
        index++;
    }
}

// استخدم الطريقة "RemoveAt" لإزالة الجزء المستنسخ عبر الفهرس.
doc->get_CustomXmlParts()->RemoveAt(1);

ASSERT_EQ(1, doc->get_CustomXmlParts()->get_Count());

// استنسخ مجموعة أجزاء XML، ثم استخدم الطريقة "Clear" لإزالة جميع عناصرها مرة واحدة.
System::SharedPtr<Aspose::Words::Markup::CustomXmlPartCollection> customXmlParts = doc->get_CustomXmlParts()->Clone();
customXmlParts->Clear();

// أنشئ علامة مستند منسقة تعرض محتويات جزءنا وأدرجها في جسم المستند.
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Block);
tag->get_XmlMapping()->SetMapping(xmlPart, u"/root[1]/text[1]", System::String::Empty);

doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(tag);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.CustomXml.docx");
```

## انظر أيضًا

* Class [CustomXmlPart](../../customxmlpart/)
* Class [CustomXmlPartCollection](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
