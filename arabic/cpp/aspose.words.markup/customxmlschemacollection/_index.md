---
title: "الفئة Aspose::Words::Markup::CustomXmlSchemaCollection"
linktitle: "CustomXmlSchemaCollection"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "الفئة Aspose::Words::Markup::CustomXmlSchemaCollection. مجموعة من السلاسل التي تمثل مخططات XML المرتبطة بجزء XML مخصص. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 7000
url: /ar/cpp/aspose.words.markup/customxmlschemacollection/
---
## CustomXmlSchemaCollection class


مجموعة من السلاسل التي تمثل مخططات XML المرتبطة بجزء XML مخصص. لمعرفة المزيد، قم بزيارة مقالة الوثائق [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/).

```cpp
class CustomXmlSchemaCollection : public System::Collections::Generic::IEnumerable<System::String>
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [Add](./add/)(const System::String\&) | يضيف عنصرًا إلى المجموعة. |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | يزيل جميع العناصر من المجموعة. |
| [Clone](./clone/)() | ينشئ نسخة عميقة من هذا الكائن. |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | يحصل على عدد العناصر الموجودة في المجموعة. |
| [GetEnumerator](./getenumerator/)() override | يرجع كائن عداد يمكن استخدامه للتنقل عبر جميع العناصر في المجموعة. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | يحصل أو يضبط العنصر في الفهرس المحدد. |
| [idx_set](./idx_set/)(int32_t, const System::String\&) | يحصل أو يضبط العنصر في الفهرس المحدد. |
| [IndexOf](./indexof/)(const System::String\&) | يرجع الفهرس الصفري للقيمة المحددة في المجموعة. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::String\&) | يزيل القيمة المحددة من المجموعة. |
| [RemoveAt](./removeat/)(int32_t) | يزيل قيمة عند الفهرس المحدد. |
| static [Type](./type/)() |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
## Typedefs

| تعريف نوع | الوصف |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |
## ملاحظات


أنت لا تنشئ مثيلات من هذه الفئة. يمكنك الوصول إلى مجموعة مخططات XML لجزء XML مخصص عبر الخاصية [Schemas](../customxmlpart/get_schemas/).

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

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
