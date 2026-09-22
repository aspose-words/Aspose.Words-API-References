---
title: "Aspose::Words::NodeCollection::RemoveAt طريقة"
linktitle: "RemoveAt"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::NodeCollection::RemoveAt طريقة. يزيل العقدة في الفهرس المحدد من المجموعة ومن المستند في C++."
type: docs
weight: 13000
url: /ar/cpp/aspose.words/nodecollection/removeat/
---
## NodeCollection::RemoveAt method


يزيل العقدة في الفهرس المحدد من المجموعة ومن المستند.

```cpp
void Aspose::Words::NodeCollection::RemoveAt(int32_t index)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| index | int32_t | الفهرس الصفري للعنصر. يُسمح بالفهارس السالبة وتُشير إلى الوصول من نهاية القائمة. على سبيل المثال، -1 يعني العنصر الأخير، -2 يعني العنصر قبل الأخير وهكذا. |

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

* Class [NodeCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
