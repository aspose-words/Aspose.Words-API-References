---
title: "Aspose::Words::Markup::IStructuredDocumentTag::get_WordOpenXML method"
linktitle: "get_WordOpenXML"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Markup::IStructuredDocumentTag::get_WordOpenXML. يحصل على سلسلة تمثل XML الموجود داخل العقدة بتنسيق FlatOpc في C++."
type: docs
weight: 13000
url: /ar/cpp/aspose.words.markup/istructureddocumenttag/get_wordopenxml/
---
## IStructuredDocumentTag::get_WordOpenXML method


يحصل على سلسلة تمثل XML الموجود داخل العقدة بتنسيق [FlatOpc](../../../aspose.words/saveformat/).

```cpp
virtual System::String Aspose::Words::Markup::IStructuredDocumentTag::get_WordOpenXML()=0
```


## أمثلة



يوضح كيفية الحصول على XML الموجود داخل العقدة بتنسيق FlatOpc.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags.docx");

System::SharedPtr<System::Collections::Generic::List<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>> tags = doc->GetChildNodes(Aspose::Words::NodeType::StructuredDocumentTag, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag> >()->LINQ_ToList();

ASSERT_TRUE(tags->idx_get(0)->get_WordOpenXML().Contains(u"<pkg:part pkg:name=\"/docProps/app.xml\" pkg:contentType=\"application/vnd.openxmlformats-officedocument.extended-properties+xml\">"));
```

## انظر أيضًا

* Interface [IStructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
