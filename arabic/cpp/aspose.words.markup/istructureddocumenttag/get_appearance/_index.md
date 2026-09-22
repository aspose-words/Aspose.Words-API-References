---
title: "Aspose::Words::Markup::IStructuredDocumentTag::get_Appearance method"
linktitle: "get_Appearance"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Markup::IStructuredDocumentTag::get_Appearance method. يحصل على مظهر العلامة المستندية المنسقة أو يضبطه في C++."
type: docs
weight: 1500
url: /ar/cpp/aspose.words.markup/istructureddocumenttag/get_appearance/
---
## IStructuredDocumentTag::get_Appearance method


يحصل أو يضبط مظهر علامة المستند المهيكلة.

```cpp
virtual Aspose::Words::Markup::SdtAppearance Aspose::Words::Markup::IStructuredDocumentTag::get_Appearance()=0
```


## أمثلة



يوضح كيفية إظهار العلامة حول المحتوى.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Multi-section structured document tags.docx");
auto tag = System::AsCast<Aspose::Words::Markup::StructuredDocumentTagRangeStart>(doc->GetChild(Aspose::Words::NodeType::StructuredDocumentTagRangeStart, 0, true));

if (tag->get_Appearance() == Aspose::Words::Markup::SdtAppearance::Hidden)
{
    tag->set_Appearance(Aspose::Words::Markup::SdtAppearance::Tags);
}
```

## انظر أيضًا

* Enum [SdtAppearance](../../sdtappearance/)
* Interface [IStructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
