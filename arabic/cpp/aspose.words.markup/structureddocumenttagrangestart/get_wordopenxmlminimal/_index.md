---
title: "طريقة Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_WordOpenXMLMinimal"
linktitle: "get_WordOpenXMLMinimal"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_WordOpenXMLMinimal. يحصل على سلسلة تمثل XML الموجود داخل العقدة بتنسيق FlatOpc. على عكس خاصية WordOpenXML، تُنشئ هذه الطريقة مستندًا مبسطًا يستبعد أي أجزاء غير متعلقة بالمحتوى في C++."
type: docs
weight: 20500
url: /ar/cpp/aspose.words.markup/structureddocumenttagrangestart/get_wordopenxmlminimal/
---
## StructuredDocumentTagRangeStart::get_WordOpenXMLMinimal method


يحصل على سلسلة تمثل XML الموجود داخل العقدة بتنسيق [FlatOpc](../../../aspose.words/saveformat/) . على عكس خاصية [WordOpenXML](../get_wordopenxml/)، تُنشئ هذه الطريقة مستندًا مبسطًا يستبعد أي أجزاء غير متعلقة بالمحتوى.

```cpp
System::String Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_WordOpenXMLMinimal()
```


## أمثلة



يوضح كيفية الحصول على XML مبسط موجود داخل العقدة بتنسيق FlatOpc.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Multi-section structured document tags.docx");
auto tag = System::AsCast<Aspose::Words::Markup::StructuredDocumentTagRangeStart>(doc->GetChild(Aspose::Words::NodeType::StructuredDocumentTagRangeStart, 0, true));

ASSERT_TRUE(tag->get_WordOpenXMLMinimal().Contains(u"<pkg:part pkg:name=\"/docProps/app.xml\" pkg:contentType=\"application/vnd.openxmlformats-officedocument.extended-properties+xml\">"));
ASSERT_FALSE(tag->get_WordOpenXMLMinimal().Contains(u"xmlns:w16cid=\"http://schemas.microsoft.com/office/word/2016/wordml/cid\""));
```

## انظر أيضًا

* Class [StructuredDocumentTagRangeStart](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
