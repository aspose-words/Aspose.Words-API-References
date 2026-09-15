---
title: "Aspose::Words::StyleCollection::get_Count طريقة"
linktitle: "get_Count"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::StyleCollection::get_Count طريقة. يحصل على عدد الأنماط في المجموعة في C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words/stylecollection/get_count/
---
## StyleCollection::get_Count method


يحصل على عدد الأنماط في المجموعة.

```cpp
int32_t Aspose::Words::StyleCollection::get_Count()
```


## أمثلة



يوضح كيفية إضافة [Style](../../style/) إلى مجموعة أنماط المستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::StyleCollection> styles = doc->get_Styles();
// تعيين المعلمات الافتراضية للأنماط الجديدة التي قد نضيفها لاحقًا إلى هذه المجموعة.
styles->get_DefaultFont()->set_Name(u"Courier New");
// إذا أضفنا نمطًا من "StyleType.Paragraph"، فإن المجموعة ستطبق القيم الخاصة بـ
// خاصية "DefaultParagraphFormat" الخاصة به إلى خاصية "ParagraphFormat" للنمط.
styles->get_DefaultParagraphFormat()->set_FirstLineIndent(15.0);
// أضف نمطًا، ثم تحقق من أنه يحتوي على الإعدادات الافتراضية.
styles->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");

ASSERT_EQ(u"Courier New", styles->idx_get(4)->get_Font()->get_Name());
ASPOSE_ASSERT_EQ(15.0, styles->idx_get(u"MyStyle")->get_ParagraphFormat()->get_FirstLineIndent());
```

## انظر أيضًا

* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
