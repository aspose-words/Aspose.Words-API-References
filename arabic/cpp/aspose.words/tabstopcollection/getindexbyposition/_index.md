---
title: "Aspose::Words::TabStopCollection::GetIndexByPosition method"
linktitle: "GetIndexByPosition"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::TabStopCollection::GetIndexByPosition method. يحصل على فهرس علامة تبويب بالموضع المحدد بالنقاط في C++."
type: docs
weight: 9000
url: /ar/cpp/aspose.words/tabstopcollection/getindexbyposition/
---
## TabStopCollection::GetIndexByPosition method


يحصل على فهرس علامة تبويب بالموضع المحدد بالنقاط.

```cpp
int32_t Aspose::Words::TabStopCollection::GetIndexByPosition(double position)
```


## أمثلة



يظهر كيفية البحث عن موضع لمعرفة ما إذا كانت علامة تبويب موجودة هناك والحصول على فهرسها.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::TabStopCollection> tabStops = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ParagraphFormat()->get_TabStops();

// أضف علامة تبويب عند موضع 30 مم.
tabStops->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(30), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);

// نتيجة "0" التي تُرجعها "GetIndexByPosition" تؤكد أن علامة تبويب
// عند 30 مم موجودة في هذه المجموعة، وهي في الفهرس 0.
ASSERT_EQ(0, tabStops->GetIndexByPosition(Aspose::Words::ConvertUtil::MillimeterToPoint(30)));

// قيمة "-1" التي تُرجعها "GetIndexByPosition" تؤكد أن
// لا توجد علامة تبويب في هذه المجموعة بموضع 60 مم.
ASSERT_EQ(-1, tabStops->GetIndexByPosition(Aspose::Words::ConvertUtil::MillimeterToPoint(60)));
```

## انظر أيضًا

* Class [TabStopCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
