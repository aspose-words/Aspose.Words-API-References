---
title: "طريقة Aspose::Words::Section::PrependContent"
linktitle: "PrependContent"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Section::PrependContent. تُدرج نسخة من محتوى القسم المصدر في بداية هذا القسم في C++."
type: docs
weight: 17000
url: /ar/cpp/aspose.words/section/prependcontent/
---
## Section::PrependContent method


يدرج نسخة من محتوى القسم المصدر في بداية هذا القسم.

```cpp
void Aspose::Words::Section::PrependContent(const System::SharedPtr<Aspose::Words::Section> &sourceSection)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| sourceSection | const System::SharedPtr\<Aspose::Words::Section\>\& | القسم الذي سيتم نسخ المحتوى منه. |
## ملاحظات


يتم نسخ محتوى [Body](../get_body/) فقط من القسم المصدر، ولا يتم نسخ إعداد الصفحة والرؤوس والتذييلات.

العُقَد تُستورد تلقائيًا إذا كان القسم المصدر ينتمي إلى مستند مختلف.

لا يتم إنشاء قسم جديد في المستند الوجهة.

## أمثلة



يظهر كيفية إلحاق محتويات قسم بآخر.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Section 1");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 2");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 3");

System::SharedPtr<Aspose::Words::Section> section = doc->get_Sections()->idx_get(2);

ASSERT_EQ(System::String(u"Section 3") + Aspose::Words::ControlChar::SectionBreak(), section->GetText());

// أدرج محتويات القسم الأول في بداية القسم الثالث.
System::SharedPtr<Aspose::Words::Section> sectionToPrepend = doc->get_Sections()->idx_get(0);
section->PrependContent(sectionToPrepend);

// أدرج محتويات القسم الثاني في نهاية القسم الثالث.
System::SharedPtr<Aspose::Words::Section> sectionToAppend = doc->get_Sections()->idx_get(1);
section->AppendContent(sectionToAppend);

// الطريقتان "PrependContent" و "AppendContent" لم تقوما بإنشاء أي أقسام جديدة.
ASSERT_EQ(3, doc->get_Sections()->get_Count());
ASSERT_EQ(System::String(u"Section 1") + Aspose::Words::ControlChar::ParagraphBreak() + u"Section 3" + Aspose::Words::ControlChar::ParagraphBreak() + u"Section 2" + Aspose::Words::ControlChar::SectionBreak(), section->GetText());
```

## انظر أيضًا

* Class [Section](../)
* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
