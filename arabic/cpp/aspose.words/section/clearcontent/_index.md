---
title: "طريقة Aspose::Words::Section::ClearContent"
linktitle: "ClearContent"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Section::ClearContent. تقوم بمسح القسم في C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words/section/clearcontent/
---
## Section::ClearContent method


يمسح القسم.

```cpp
void Aspose::Words::Section::ClearContent()
```

## ملاحظات


يتم مسح نص [Body](../get_body/)، ويُترك فقرة فارغة واحدة تمثل فاصل القسم.

يتم مسح نص جميع الرؤوس والتذييلات، لكن كائنات [HeaderFooter](../../headerfooter/) نفسها لا تُزال.

## أمثلة



يوضح كيفية مسح محتويات القسم.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Hello world!");

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
ASSERT_EQ(1, doc->get_FirstSection()->get_Body()->get_Paragraphs()->get_Count());

// تشغيل طريقة "ClearContent" سيزيل جميع محتويات القسم
// ولكن سيترك فقرة فارغة لإضافة المحتوى مرة أخرى.
doc->get_FirstSection()->ClearContent();

ASSERT_EQ(System::String::Empty, doc->GetText().Trim());
ASSERT_EQ(1, doc->get_FirstSection()->get_Body()->get_Paragraphs()->get_Count());
```

## انظر أيضًا

* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
