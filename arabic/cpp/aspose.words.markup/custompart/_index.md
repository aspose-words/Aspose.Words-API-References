---
title: "فئة Aspose::Words::Markup::CustomPart"
linktitle: "CustomPart"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Markup::CustomPart class. يمثل جزءًا مخصصًا (محتوى تعسفي) غير معرف وفقًا لمعيار ISO/IEC 29500. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 1000
url: /ar/cpp/aspose.words.markup/custompart/
---
## CustomPart class


يمثل جزءًا مخصصًا (محتوى تعسفي) غير معرف بمعيار ISO/IEC 29500. لمعرفة المزيد، قم بزيارة مقالة الوثائق [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/).

```cpp
class CustomPart : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [Clone](./clone/)() | ينشئ نسخة "عميقة بما فيه الكفاية" من الكائن. لا يكرر بايتات قيمة [Data](./get_data/). |
| [CustomPart](./custompart/)() |  |
| [get_ContentType](./get_contenttype/)() const | يحدد نوع المحتوى لهذا الجزء المخصص. |
| [get_Data](./get_data/)() const | يحتوي على بيانات هذا الجزء المخصص. |
| [get_IsExternal](./get_isexternal/)() const | خطأ إذا تم تخزين هذا الجزء المخصص داخل حزمة OOXML. صحيح إذا كان هذا الجزء المخصص هدفًا خارجيًا. |
| [get_Name](./get_name/)() const | يحصل أو يعيّن الاسم المطلق لهذا الجزء داخل حزمة OOXML أو عنوان URL الهدف. |
| [get_RelationshipType](./get_relationshiptype/)() const | يحصل أو يعيّن نوع العلاقة من الجزء الأب إلى هذا الجزء المخصص. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_ContentType](./set_contenttype/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Markup::CustomPart::get_ContentType](./get_contenttype/). |
| [set_Data](./set_data/)(const System::ArrayPtr\<uint8_t\>\&) | مُعيّن لـ [Aspose::Words::Markup::CustomPart::get_Data](./get_data/). |
| [set_IsExternal](./set_isexternal/)(bool) | مُعيّن لـ [Aspose::Words::Markup::CustomPart::get_IsExternal](./get_isexternal/). |
| [set_Name](./set_name/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Markup::CustomPart::get_Name](./get_name/). |
| [set_RelationshipType](./set_relationshiptype/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Markup::CustomPart::get_RelationshipType](./get_relationshiptype/). |
| static [Type](./type/)() |  |
## ملاحظات


تمثل هذه الفئة جزء OOXML هو هدف "علاقة غير معروفة". جميع العلاقات غير المعرفة ضمن ISO/IEC 29500 تُعتبر "علاقات غير معروفة". تُسمح بالعلاقات غير المعروفة داخل مستند Office Open XML بشرط أن تتوافق مع إرشادات ترميز العلاقات.

يحافظ Microsoft Word على الأجزاء المخصصة أثناء دورات الفتح/الحفظ. يمكن العثور على بعض المعلومات الإضافية هنا [http://blogs.msdn.com/dmahugh/archive/2006/11/25/arbitrary-content-in-an-opc-package.aspx](http://blogs.msdn.com/dmahugh/archive/2006/11/25/arbitrary-content-in-an-opc-package.aspx)

يقوم Aspose.Words أيضًا بنقل الأجزاء المخصصة ذهابًا وإيابًا، بالإضافة إلى ذلك، يسمح بالوصول برمجيًا إلى هذه الأجزاء عبر كائنات [CustomPart](./) و[CustomPartCollection](../custompartcollection/).

لا تخلط بين الأجزاء المخصصة وبيانات XML المخصصة. استخدم [CustomXmlPart](../customxmlpart/) إذا كنت بحاجة للوصول إلى بيانات XML المخصصة.

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

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
