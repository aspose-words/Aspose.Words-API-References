---
title: "Aspose::Words::TabStopCollection::get_Count method"
linktitle: "get_Count"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::TabStopCollection::get_Count method. يحصل على عدد علامات التبويب في المجموعة في C++."
type: docs
weight: 7000
url: /ar/cpp/aspose.words/tabstopcollection/get_count/
---
## TabStopCollection::get_Count method


يحصل على عدد علامات التبويب في المجموعة.

```cpp
int32_t Aspose::Words::TabStopCollection::get_Count()
```


## أمثلة



يوضح كيفية العمل مع مجموعة علامات التبويب في المستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::TabStopCollection> tabStops = builder->get_ParagraphFormat()->get_TabStops();

// 72 نقطة هي "بوصة" واحدة على مسطرة علامات التبويب في Microsoft Word.
tabStops->Add(System::MakeObject<Aspose::Words::TabStop>(72.0));
tabStops->Add(System::MakeObject<Aspose::Words::TabStop>(432.0, Aspose::Words::TabAlignment::Right, Aspose::Words::TabLeader::Dashes));

ASSERT_EQ(2, tabStops->get_Count());
ASSERT_FALSE(tabStops->idx_get(0)->get_IsClear());
ASSERT_FALSE(System::ObjectExt::Equals(tabStops->idx_get(0), tabStops->idx_get(1)));

// كل حرف "tab" ينقل مؤشر المُنشئ إلى موقع علامة التبويب التالية.
builder->Writeln(u"Start\tTab 1\tTab 2");

System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

ASSERT_EQ(2, paragraphs->get_Count());

// كل فقرة تحصل على مجموعة علامات التبويب الخاصة بها، التي تستنسخ قيمها من مجموعة علامات التبويب الخاصة بمنشئ المستند.
ASPOSE_ASSERT_EQ(paragraphs->idx_get(0)->get_ParagraphFormat()->get_TabStops(), paragraphs->idx_get(1)->get_ParagraphFormat()->get_TabStops());
ASPOSE_ASSERT_NS(paragraphs->idx_get(0)->get_ParagraphFormat()->get_TabStops(), paragraphs->idx_get(1)->get_ParagraphFormat()->get_TabStops());

// مجموعة علامات التبويب يمكن أن تشير إلى TabStops قبل وبعد مواضع معينة.
ASPOSE_ASSERT_EQ(72.0, tabStops->Before(100.0)->get_Position());
ASPOSE_ASSERT_EQ(432.0, tabStops->After(100.0)->get_Position());

// يمكننا مسح مجموعة علامات التبويب للفقرة للعودة إلى سلوك التبويب الافتراضي.
paragraphs->idx_get(1)->get_ParagraphFormat()->get_TabStops()->Clear();

ASSERT_EQ(0, paragraphs->idx_get(1)->get_ParagraphFormat()->get_TabStops()->get_Count());

doc->Save(get_ArtifactsDir() + u"TabStopCollection.TabStopCollection.docx");
```

## انظر أيضًا

* Class [TabStopCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
