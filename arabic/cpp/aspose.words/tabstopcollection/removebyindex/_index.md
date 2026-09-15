---
title: "Aspose::Words::TabStopCollection::RemoveByIndex طريقة"
linktitle: "RemoveByIndex"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::TabStopCollection::RemoveByIndex طريقة. يزيل علامة تبويب في الفهرس المحدد من المجموعة في C++."
type: docs
weight: 14000
url: /ar/cpp/aspose.words/tabstopcollection/removebyindex/
---
## TabStopCollection::RemoveByIndex method


يزيل علامة تبويب عند الفهرس المحدد من المجموعة.

```cpp
void Aspose::Words::TabStopCollection::RemoveByIndex(int32_t index)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| index | int32_t | فهرس داخل مجموعة علامات التبويب. |

## أمثلة



يوضح كيفية اختيار علامة تبويب في مستند حسب فهرسه وإزالتها.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::TabStopCollection> tabStops = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ParagraphFormat()->get_TabStops();

tabStops->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(30), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);
tabStops->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(60), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);

ASSERT_EQ(2, tabStops->get_Count());

// إزالة أول علامة تبويب.
tabStops->RemoveByIndex(0);

ASSERT_EQ(1, tabStops->get_Count());

doc->Save(get_ArtifactsDir() + u"TabStopCollection.RemoveByIndex.docx");
```

## انظر أيضًا

* Class [TabStopCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
