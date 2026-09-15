---
title: "Aspose::Words::StyleCollection::get_DefaultFont طريقة"
linktitle: "get_DefaultFont"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::StyleCollection::get_DefaultFont طريقة. يحصل على تنسيق النص الافتراضي للمستند في C++."
type: docs
weight: 6000
url: /ar/cpp/aspose.words/stylecollection/get_defaultfont/
---
## StyleCollection::get_DefaultFont method


يحصل على تنسيق النص الافتراضي للمستند.

```cpp
System::SharedPtr<Aspose::Words::Font> Aspose::Words::StyleCollection::get_DefaultFont()
```

## ملاحظات


لاحظ أن الإعدادات الافتراضية على مستوى المستند تم تقديمها في Microsoft Word 2007 وتدعم بالكامل في صيغ OOXML ([Docx](../../loadformat/)) فقط. صيغ المستندات السابقة لديها دعم محدود لهذه الميزة ويمكن فقط تخزين أسماء الخطوط.

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

* Class [Font](../../font/)
* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
