---
title: "Aspose::Words::Markup::CustomXmlSchemaCollection::IndexOf طريقة"
linktitle: "IndexOf"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Markup::CustomXmlSchemaCollection::IndexOf طريقة. تُرجِع الفهرس الصفري للقيمة المحددة في المجموعة في C++."
type: docs
weight: 14000
url: /ar/cpp/aspose.words.markup/customxmlschemacollection/indexof/
---
## CustomXmlSchemaCollection::IndexOf method


يرجع الفهرس الصفري للقيمة المحددة في المجموعة.

```cpp
int32_t Aspose::Words::Markup::CustomXmlSchemaCollection::IndexOf(const System::String &value)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| value | const System::String\& | القيمة الحساسة لحالة الأحرف للعثور عليها. |

### ReturnValue

الفهرس الصفري. قيمة سلبية إذا لم يُعثر عليه.

## أمثلة



يظهر كيفية العمل مع مجموعة مخططات XML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::String xmlPartId = System::Guid::NewGuid().ToString(u"B");
System::String xmlPartContent = u"<root><text>Hello, World!</text></root>";
System::SharedPtr<Aspose::Words::Markup::CustomXmlPart> xmlPart = doc->get_CustomXmlParts()->Add(xmlPartId, xmlPartContent);

// أضف ارتباط مخطط XML.
xmlPart->get_Schemas()->Add(u"http://www.w3.org/2001/XMLSchema");

// انسخ مجموعة ارتباط مخطط XML لجزء XML المخصص،
// ثم أضف بعض المخططات الجديدة إلى النسخة.
System::SharedPtr<Aspose::Words::Markup::CustomXmlSchemaCollection> schemas = xmlPart->get_Schemas()->Clone();
schemas->Add(u"http://www.w3.org/2001/XMLSchema-instance");
schemas->Add(u"http://schemas.microsoft.com/office/2006/metadata/contentType");

ASSERT_EQ(3, schemas->get_Count());
ASSERT_EQ(2, schemas->IndexOf(u"http://schemas.microsoft.com/office/2006/metadata/contentType"));

// قم بتعداد المخططات واطبع كل عنصر.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::String>> enumerator = schemas->GetEnumerator();
    while (enumerator->MoveNext())
    {
        std::cout << enumerator->get_Current() << std::endl;
    }
}

// فيما يلي ثلاث طرق لإزالة المخططات من المجموعة.
// 1 -  إزالة مخطط حسب الفهرس:
schemas->RemoveAt(2);

// 2 -  إزالة مخطط حسب القيمة:
schemas->Remove(u"http://www.w3.org/2001/XMLSchema");

// 3 - استخدم طريقة "Clear" لتفريغ المجموعة مرة واحدة.
schemas->Clear();

ASSERT_EQ(0, schemas->get_Count());
```

## انظر أيضًا

* Class [CustomXmlSchemaCollection](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
