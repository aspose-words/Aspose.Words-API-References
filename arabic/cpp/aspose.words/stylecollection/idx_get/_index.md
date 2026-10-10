---
title: "Aspose::Words::StyleCollection::idx_get طريقة"
linktitle: "idx_get"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::StyleCollection::idx_get طريقة. يحصل على نمط مدمج بواسطة معرّفه المستقل عن اللغة في C++."
type: docs
weight: 11000
url: /ar/cpp/aspose.words/stylecollection/idx_get/
---
## StyleCollection::idx_get(Aspose::Words::StyleIdentifier) method


يحصل على نمط مدمج بواسطة معرفه المستقل عن اللغة.

```cpp
System::SharedPtr<Aspose::Words::Style> Aspose::Words::StyleCollection::idx_get(Aspose::Words::StyleIdentifier sti)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| sti | Aspose::Words::StyleIdentifier | قيمة [StyleIdentifier](../../styleidentifier/) التي تحدد النمط المدمج المراد استرجاعه. |
## ملاحظات


عند الوصول إلى نمط غير موجود بعد، يتم إنشاؤه تلقائيًا.

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

* Class [Style](../../style/)
* Enum [StyleIdentifier](../../styleidentifier/)
* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## StyleCollection::idx_get(const System::String\&) method


يحصل على نمط بالاسم أو الاسم المستعار.

```cpp
System::SharedPtr<Aspose::Words::Style> Aspose::Words::StyleCollection::idx_get(const System::String &name)
```

## ملاحظات


حسّاس لحالة الأحرف، يرجع **null** إذا لم يتم العثور على النمط بالاسم المحدد.

إذا كان هذا اسمًا إنجليزيًا لنمط مدمج غير موجود بعد، يتم إنشاؤه تلقائيًا.

## أمثلة



يظهر متى يجب إعادة حساب تخطيط الصفحة للمستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// حفظ المستند إلى PDF أو إلى صورة أو طباعته للمرة الأولى سيؤدي تلقائيًا
// لتخزين تخطيط المستند داخل صفحاته في الذاكرة المؤقتة.
doc->Save(get_ArtifactsDir() + u"Document.UpdatePageLayout.1.pdf");

// تعديل المستند بطريقة ما.
doc->get_Styles()->idx_get(u"Normal")->get_Font()->set_Size(6);
doc->get_Sections()->idx_get(0)->get_PageSetup()->set_Orientation(Aspose::Words::Orientation::Landscape);
doc->get_Sections()->idx_get(0)->get_PageSetup()->set_Margins(Aspose::Words::Margins::Mirrored);

// في الإصدار الحالي من Aspose.Words، تعديل المستند لا يعيد بناءه تلقائيًا
// تخطيط الصفحة المخزّن مؤقتًا. إذا أردنا أن يكون التخطيط المخزّن مؤقتًا
// للبقاء محدثًا، سنحتاج إلى تحديثه يدويًا.
doc->UpdatePageLayout();

doc->Save(get_ArtifactsDir() + u"Document.UpdatePageLayout.2.pdf");
```

## انظر أيضًا

* Class [Style](../../style/)
* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## StyleCollection::idx_get(int32_t) method


يحصل على نمط حسب الفهرس.

```cpp
System::SharedPtr<Aspose::Words::Style> Aspose::Words::StyleCollection::idx_get(int32_t index)
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

* Class [Style](../../style/)
* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
