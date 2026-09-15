---
title: "Aspose::Words::TabStopCollection::GetPositionByIndex method"
linktitle: "GetPositionByIndex"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::TabStopCollection::GetPositionByIndex method. يحصل على الموضع (بالنقاط) لعلامة التبويب عند الفهرس المحدد في C++."
type: docs
weight: 10000
url: /ar/cpp/aspose.words/tabstopcollection/getpositionbyindex/
---
## TabStopCollection::GetPositionByIndex method


يحصل على موضع (بالنقاط) علامة التبويب عند الفهرس المحدد.

```cpp
double Aspose::Words::TabStopCollection::GetPositionByIndex(int32_t index)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| index | int32_t | فهرس داخل مجموعة علامات التبويب. |

### ReturnValue

موضع علامة التبويب.

## أمثلة



يظهر كيفية العثور على علامة تبويب بواسطة فهرسها والتحقق من موضعها.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::TabStopCollection> tabStops = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ParagraphFormat()->get_TabStops();

tabStops->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(30), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);
tabStops->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(60), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);

// تحقق من موضع علامة التبويب الثانية في المجموعة.
ASSERT_NEAR(Aspose::Words::ConvertUtil::MillimeterToPoint(60), tabStops->GetPositionByIndex(1), 0.1);
```

## انظر أيضًا

* Class [TabStopCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
