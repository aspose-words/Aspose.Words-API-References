---
title: "Aspose::Words::Properties::DocumentPropertyCollection::GetEnumerator طريقة"
linktitle: "GetEnumerator"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Properties::DocumentPropertyCollection::GetEnumerator طريقة. تُرجع كائن عداد يمكن استخدامه للتنقل عبر جميع العناصر في المجموعة في C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words.properties/documentpropertycollection/getenumerator/
---
## DocumentPropertyCollection::GetEnumerator method


يرجع كائن عداد يمكن استخدامه للتنقل عبر جميع العناصر في المجموعة.

```cpp
System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Properties::DocumentProperty>>> Aspose::Words::Properties::DocumentPropertyCollection::GetEnumerator() override
```


## أمثلة



يظهر كيفية التعامل مع خصائص المستند المخصصة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Properties::CustomDocumentProperties> properties = doc->get_CustomDocumentProperties();

ASSERT_EQ(0, properties->get_Count());

// خصائص المستند المخصصة هي أزواج مفتاح-قيمة يمكننا إضافتها إلى المستند.
properties->Add(u"Authorized", true);
properties->Add(u"Authorized By", System::String(u"John Doe"));
properties->Add(u"Authorized Date", System::DateTime::get_Today());
properties->Add(u"Authorized Revision", doc->get_BuiltInDocumentProperties()->get_RevisionNumber());
properties->Add(u"Authorized Amount", 123.45);

// المجموعة ترتب الخصائص المخصصة بترتيب أبجدي.
ASSERT_EQ(1, properties->IndexOf(u"Authorized Amount"));
ASSERT_EQ(5, properties->get_Count());

// اطبع كل خاصية مخصصة في المستند.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Properties::DocumentProperty>>> enumerator = properties->GetEnumerator();
    while (enumerator->MoveNext())
    {
        std::cout << System::String::Format(u"Name: \"{0}\"\n\tType: \"{1}\"\n\tValue: \"{2}\"", enumerator->get_Current()->get_Name(), enumerator->get_Current()->get_Type(), enumerator->get_Current()->get_Value()) << std::endl;
    }
}

// اعرض قيمة خاصية مخصصة باستخدام حقل DOCPROPERTY.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldDocProperty>(builder->InsertField(u" DOCPROPERTY \"Authorized By\""));
field->Update();

ASSERT_EQ(u"John Doe", field->get_Result());

// يمكننا العثور على هذه الخصائص المخصصة في Microsoft Word عبر "File" -> "Properties" > "Advanced Properties" > "Custom".
doc->Save(get_ArtifactsDir() + u"DocumentProperties.DocumentPropertyCollection.docx");

// فيما يلي ثلاث طرق لإزالة الخصائص المخصصة من مستند.
// 1 -  إزالة حسب الفهرس:
properties->RemoveAt(1);

ASSERT_FALSE(properties->Contains(u"Authorized Amount"));
ASSERT_EQ(4, properties->get_Count());

// 2 -  إزالة حسب الاسم:
properties->Remove(u"Authorized Revision");

ASSERT_FALSE(properties->Contains(u"Authorized Revision"));
ASSERT_EQ(3, properties->get_Count());

// 3 -  إفراغ المجموعة بالكامل مرة واحدة:
properties->Clear();

ASSERT_EQ(0, properties->get_Count());
```

## انظر أيضًا

* Class [DocumentProperty](../../documentproperty/)
* Class [DocumentPropertyCollection](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
