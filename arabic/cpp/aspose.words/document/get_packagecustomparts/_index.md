---
title: "طريقة Aspose::Words::Document::get_PackageCustomParts"
linktitle: "get_PackageCustomParts"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Document::get_PackageCustomParts. يحصل أو يضبط مجموعة الأجزاء المخصصة (محتوى تعسفي) المرتبطة بحزمة OOXML باستخدام \\\"unknown relationships\\\" في C++."
type: docs
weight: 42000
url: /ar/cpp/aspose.words/document/get_packagecustomparts/
---
## Document::get_PackageCustomParts method


يحصل على أو يضبط مجموعة الأجزاء المخصصة (محتوى تعسفي) المرتبطة بحزمة OOXML باستخدام \"علاقات غير معروفة\".

```cpp
System::SharedPtr<Aspose::Words::Markup::CustomPartCollection> Aspose::Words::Document::get_PackageCustomParts() const
```

## ملاحظات


لا تخلط بين هذه الأجزاء المخصصة وبيانات XML المخصصة. إذا كنت بحاجة للوصول إلى أجزاء XML المخصصة، استخدم الخاصية [CustomXmlParts](../get_customxmlparts/).

تحتوي هذه المجموعة على أجزاء OOXML التي يكون الأصل لها حزمة OOXML وتستهدف \"unknown relationship\". لمزيد من المعلومات راجع [CustomPart](../../../aspose.words.markup/custompart/).

يقوم Aspose.Words بتحميل وحفظ الأجزاء المخصصة في مستندات OOXML فقط.

هذه الخاصية لا يمكن أن تكون **null**.

## أمثلة



يظهر كيفية الوصول إلى مجموعة الأجزاء المخصصة التعسفية في المستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Custom parts OOXML package.docx");

ASSERT_EQ(2, doc->get_PackageCustomParts()->get_Count());

// استنسخ الجزء الثاني، ثم أضف النسخة إلى المجموعة.
System::SharedPtr<Aspose::Words::Markup::CustomPart> clonedPart = doc->get_PackageCustomParts()->idx_get(1)->Clone();
doc->get_PackageCustomParts()->Add(clonedPart);

ASSERT_EQ(3, doc->get_PackageCustomParts()->get_Count());

// قم بالتعداد عبر المجموعة واطبع كل جزء.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Markup::CustomPart>>> enumerator = doc->get_PackageCustomParts()->GetEnumerator();
    int32_t index = 0;
    while (enumerator->MoveNext())
    {
        std::cout << System::String::Format(u"Part index {0}:", index) << std::endl;
        std::cout << System::String::Format(u"\tName:\t\t\t\t{0}", enumerator->get_Current()->get_Name()) << std::endl;
        std::cout << System::String::Format(u"\tContent type:\t\t{0}", enumerator->get_Current()->get_ContentType()) << std::endl;
        std::cout << System::String::Format(u"\tRelationship type:\t{0}", enumerator->get_Current()->get_RelationshipType()) << std::endl;
        std::cout << (enumerator->get_Current()->get_IsExternal() ? u"\tSourced from outside the document" : System::String::Format(u"\tStored within the document, length: {0} bytes", enumerator->get_Current()->get_Data()->get_Length())) << std::endl;
        index++;
    }
}

// يمكننا إزالة العناصر من هذه المجموعة بشكل فردي، أو جميعها مرة واحدة.
doc->get_PackageCustomParts()->RemoveAt(2);

ASSERT_EQ(2, doc->get_PackageCustomParts()->get_Count());

doc->get_PackageCustomParts()->Clear();

ASSERT_EQ(0, doc->get_PackageCustomParts()->get_Count());
```

## انظر أيضًا

* Class [CustomPartCollection](../../../aspose.words.markup/custompartcollection/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
