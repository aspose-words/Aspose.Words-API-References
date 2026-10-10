---
title: "Aspose::Words::Comparing::AdvancedCompareOptions class"
linktitle: "AdvancedCompareOptions"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Comparing::AdvancedCompareOptions class. يسمح بتعيين خيارات مقارنة متقدمة في C++."
type: docs
weight: 500
url: /ar/cpp/aspose.words.comparing/advancedcompareoptions/
---
## AdvancedCompareOptions class


يسمح بتعيين خيارات مقارنة متقدمة.

```cpp
class AdvancedCompareOptions : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [AdvancedCompareOptions](./advancedcompareoptions/)() |  |
| [get_IgnoreDmlUniqueId](./get_ignoredmluniqueid/)() const | يحدد ما إذا كان يجب تجاهل الاختلاف في المعرف الفريد لـ DrawingML. |
| [get_IgnoreStoreItemId](./get_ignorestoreitemid/)() const | يحدد ما إذا كان يجب تجاهل الاختلاف في معرف عنصر التخزين لـ StructuredDocumentTag. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_IgnoreDmlUniqueId](./set_ignoredmluniqueid/)(bool) | دالة ضبط لـ [Aspose::Words::Comparing::AdvancedCompareOptions::get_IgnoreDmlUniqueId](./get_ignoredmluniqueid/). |
| [set_IgnoreStoreItemId](./set_ignorestoreitemid/)(bool) | دالة ضبط لـ [Aspose::Words::Comparing::AdvancedCompareOptions::get_IgnoreStoreItemId](./get_ignorestoreitemid/). |
| static [Type](./type/)() |  |

## أمثلة



يوضح كيفية مقارنة SDT بنفس المحتوى ولكن بمعرف عنصر تخزين مختلف.
```cpp
auto docA = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document with SDT 1.docx");
auto docB = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document with SDT 2.docx");

// قم بتكوين الخيارات لمقارنة SDT بنفس المحتوى ولكن بمعرف عنصر تخزين مختلف.
auto compareOptions = System::MakeObject<Aspose::Words::Comparing::CompareOptions>();
compareOptions->get_AdvancedOptions()->set_IgnoreStoreItemId(false);

docA->Compare(docB, u"user", System::DateTime::get_Now(), compareOptions);
ASSERT_EQ(8, docA->get_Revisions()->get_Count());

compareOptions->get_AdvancedOptions()->set_IgnoreStoreItemId(true);

docA->get_Revisions()->RejectAll();
docA->Compare(docB, u"user", System::DateTime::get_Now(), compareOptions);
ASSERT_EQ(0, docA->get_Revisions()->get_Count());
```

## انظر أيضًا

* Namespace [Aspose::Words::Comparing](../)
* Library [Aspose.Words for C++](../../)
