---
title: "فئة Aspose::Words::TabStopCollection"
linktitle: "TabStopCollection"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::TabStopCollection. مجموعة من كائنات TabStop التي تمثل علامات تبويب مخصصة لفقرة أو نمط. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 69000
url: /ar/cpp/aspose.words/tabstopcollection/
---
## TabStopCollection class


مجموعة من كائنات [TabStop](../tabstop/) التي تمثل علامات تبويب مخصصة لفقرة أو نمط. لمعرفة المزيد، زر مقالة الوثائق [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/).

```cpp
class TabStopCollection : public Aspose::Words::InternableComplexAttr,
                          public Aspose::Words::IExpandableAttr
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::TabStop\>\&) | يضيف أو يستبدل علامة تبويب في المجموعة. |
| [Add](./add/)(double, Aspose::Words::TabAlignment, Aspose::Words::TabLeader) | يضيف أو يستبدل علامة تبويب في المجموعة. |
| [After](./after/)(double) | يحصل على أول علامة تبويب إلى يمين الموضع المحدد. |
| [Before](./before/)(double) | يحصل على أول علامة تبويب إلى يسار الموضع المحدد. |
| [Clear](./clear/)() | يحذف جميع مواضع علامات التبويب. |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::TabStopCollection\>\&) | يحدد ما إذا كانت [TabStopCollection](./) المحددة مساوية في القيمة إلى [TabStopCollection](./) الحالية. |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | يحدد ما إذا كان الكائن المحدد مساوٍ في القيمة للكائن الحالي. |
| [get_Count](./get_count/)() | يحصل على عدد علامات التبويب في المجموعة. |
| [GetHashCode](./gethashcode/)() const override | يعمل كدالة تجزئة لهذا النوع. |
| [GetIndexByPosition](./getindexbyposition/)(double) | يحصل على فهرس علامة تبويب بالموضع المحدد بالنقاط. |
| [GetPositionByIndex](./getpositionbyindex/)(int32_t) | يحصل على موضع (بالنقاط) علامة التبويب عند الفهرس المحدد. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | يحصل على علامة تبويب عند الفهرس المعطى. |
| [idx_get](./idx_get/)(double) | يحصل على علامة تبويب عند الموضع المحدد. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [RemoveByIndex](./removebyindex/)(int32_t) | يزيل علامة تبويب عند الفهرس المحدد من المجموعة. |
| [RemoveByPosition](./removebyposition/)(double) | يزيل علامة تبويب عند الموضع المحدد من المجموعة. |
| static [Type](./type/)() |  |
## ملاحظات


في مستندات Microsoft Word، يمكن تعريف علامة تبويب في خصائص نمط الفقرة أو مباشرةً في خصائص الفقرة. يمكن أن يكون النمط مبنيًا على نمط آخر. لذلك، مجموعة علامات التبويب الكاملة لكائن معين هي مزيج من علامات التبويب المعرفة مباشرةً على هذا الكائن وعلامات التبويب الموروثة من الأنماط الأم.

في Aspose.Words، عندما تحصل على [TabStopCollection](./) لفقرة أو نمط، فإنها تحتوي فقط على علامات التبويب المخصصة المعرفة مباشرةً لهذه الفقرة أو النمط. المجموعة لا تشمل علامات التبويب المعرفة في الأنماط الأم أو علامات التبويب الافتراضية.

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

* Class [InternableComplexAttr](../internablecomplexattr/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
