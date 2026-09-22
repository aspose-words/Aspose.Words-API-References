---
title: "Aspose::Words::Markup::IStructuredDocumentTag::RemoveSelfOnly method"
linktitle: "RemoveSelfOnly"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Markup::IStructuredDocumentTag::RemoveSelfOnly method. يزيل هذا العقدة SDT نفسها فقط، لكنه يحتفظ بالمحتوى داخل شجرة المستند في C++."
type: docs
weight: 17500
url: /ar/cpp/aspose.words.markup/istructureddocumenttag/removeselfonly/
---
## IStructuredDocumentTag::RemoveSelfOnly method


يزيل عقدة الـ SDT هذه فقط، لكنه يحتفظ بمحتواها داخل شجرة المستند.

```cpp
virtual void Aspose::Words::Markup::IStructuredDocumentTag::RemoveSelfOnly()=0
```


## أمثلة



يُظهر كيفية إزالة علامة المستند المُنظمة، لكنه يحتفظ بالمحتوى داخلها.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags.docx");

// توفر هذه المجموعة واجهة موحدة للوصول إلى العلامات المُنظمة ذات النطاق وغير ذات النطاق.
System::SharedPtr<System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Markup::IStructuredDocumentTag>>> sdts = doc->get_Range()->get_StructuredDocumentTags()->LINQ_ToList();
ASSERT_EQ(5, sdts->LINQ_Count());

// هنا يمكننا الحصول على العقد الفرعية من الواجهة المشتركة للعلامات المُنظمة ذات النطاق وغير ذات النطاق.
for (auto&& sdt : System::IterateOver(sdts))
{
    if (sdt->GetChildNodes(Aspose::Words::NodeType::Any, false)->get_Count() > 0)
    {
        sdt->RemoveSelfOnly();
    }
}

sdts = doc->get_Range()->get_StructuredDocumentTags()->LINQ_ToList();
ASSERT_EQ(0, sdts->LINQ_Count());
```

## انظر أيضًا

* Interface [IStructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
