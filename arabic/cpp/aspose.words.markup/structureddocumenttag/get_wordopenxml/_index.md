---
title: "طريقة Aspose::Words::Markup::StructuredDocumentTag::get_WordOpenXML"
linktitle: "get_WordOpenXML"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Markup::StructuredDocumentTag::get_WordOpenXML. يحصل على سلسلة تمثل XML الموجود داخل العقدة بتنسيق FlatOpc في C++."
type: docs
weight: 33000
url: /ar/cpp/aspose.words.markup/structureddocumenttag/get_wordopenxml/
---
## StructuredDocumentTag::get_WordOpenXML method


يحصل على سلسلة تمثل XML الموجود داخل العقدة بتنسيق [FlatOpc](../../../aspose.words/saveformat/).

```cpp
System::String Aspose::Words::Markup::StructuredDocumentTag::get_WordOpenXML() override
```


## أمثلة



يوضح كيفية الحصول على XML الموجود داخل العقدة بتنسيق FlatOpc.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags.docx");

System::SharedPtr<System::Collections::Generic::List<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>> tags = doc->GetChildNodes(Aspose::Words::NodeType::StructuredDocumentTag, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag> >()->LINQ_ToList();

ASSERT_TRUE(tags->idx_get(0)->get_WordOpenXML().Contains(u"<pkg:part pkg:name=\"/docProps/app.xml\" pkg:contentType=\"application/vnd.openxmlformats-officedocument.extended-properties+xml\">"));
```

## انظر أيضًا

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
