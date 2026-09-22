---
title: "طريقة Aspose::Words::Section::Clone"
linktitle: "Clone"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Section::Clone. تنشئ نسخة مكررة من هذا القسم في C++."
type: docs
weight: 7000
url: /ar/cpp/aspose.words/section/clone/
---
## Section::Clone method


ينشئ نسخة مكررة من هذا القسم.

```cpp
System::SharedPtr<Aspose::Words::Section> Aspose::Words::Section::Clone()
```


## أمثلة



يوضح كيفية إضافة وإزالة الأقسام في مستند
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Section 1");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 2");

ASSERT_EQ(u"Section 1\x000c" u"Section 2", doc->GetText().Trim());

// احذف القسم الأول من المستند
doc->get_Sections()->RemoveAt(0);

ASSERT_EQ(u"Section 2", doc->GetText().Trim());

// أضف نسخة من ما هو الآن القسم الأول إلى نهاية المستند
int32_t lastSectionIdx = doc->get_Sections()->get_Count() - 1;
System::SharedPtr<Aspose::Words::Section> newSection = doc->get_Sections()->idx_get(lastSectionIdx)->Clone();
doc->get_Sections()->Add(newSection);

ASSERT_EQ(u"Section 2\x000c" u"Section 2", doc->GetText().Trim());
```

## انظر أيضًا

* Class [Section](../)
* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
