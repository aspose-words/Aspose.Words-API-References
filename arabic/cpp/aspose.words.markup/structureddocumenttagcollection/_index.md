---
title: "فئة Aspose::Words::Markup::StructuredDocumentTagCollection"
linktitle: "StructuredDocumentTagCollection"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::Markup::StructuredDocumentTagCollection. مجموعة من مثيلات IStructuredDocumentTag التي تمثل علامات المستند المهيكلة في النطاق المحدد. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 12000
url: /ar/cpp/aspose.words.markup/structureddocumenttagcollection/
---
## StructuredDocumentTagCollection class


مجموعة من مثيلات [IStructuredDocumentTag](../istructureddocumenttag/) التي تمثل علامات المستند المهيكلة في النطاق المحدد. لمعرفة المزيد، زر مقالة الوثائق [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/).

```cpp
class StructuredDocumentTagCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Markup::IStructuredDocumentTag>>
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_Count](./get_count/)() | يعيد عدد علامات المستند المهيكلة في المجموعة. |
| [GetById](./getbyid/)(int32_t) | يعيد علامة المستند المهيكلة حسب المعرف. |
| [GetByTag](./getbytag/)(const System::String\&) | يعيد أول علامة مستند مهيكلة يتم العثور عليها في المجموعة بالوسم المحدد. |
| [GetByTitle](./getbytitle/)(const System::String\&) | يعيد أول علامة مستند مهيكلة يتم العثور عليها في المجموعة بالعنوان المحدد. |
| [GetEnumerator](./getenumerator/)() override | يرجع كائن عدّاد. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | يعيد علامة المستند المهيكلة عند الفهرس المحدد. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(int32_t) | يزيل علامة المستند المهيكلة بالمعرف المحدد. |
| [RemoveAt](./removeat/)(int32_t) | يزيل علامة مستند مهيكلة عند الفهرس المحدد. |
| static [Type](./type/)() |  |

## أمثلة



يوضح كيفية الحصول على علامة المستند المهيكلة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags by id.docx");

// احصل على علامة المستند المهيكلة حسب المعرف.
System::SharedPtr<Aspose::Words::Markup::IStructuredDocumentTag> sdt = doc->get_Range()->get_StructuredDocumentTags()->GetById(1160505028);
std::cout << System::Convert::ToString(sdt->get_IsMultiSection()) << std::endl;
std::cout << sdt->get_Title() << std::endl;

// احصل على علامة المستند المهيكلة أو العلامة المتقاربة حسب العنوان.
sdt = doc->get_Range()->get_StructuredDocumentTags()->GetByTitle(u"Alias4");
std::cout << sdt->get_Id() << std::endl;
```

## انظر أيضًا

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
