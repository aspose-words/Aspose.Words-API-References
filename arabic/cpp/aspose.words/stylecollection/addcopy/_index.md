---
title: "طريقة Aspose::Words::StyleCollection::AddCopy"
linktitle: "AddCopy"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::StyleCollection::AddCopy. تنسخ نمطًا إلى هذه المجموعة في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words/stylecollection/addcopy/
---
## StyleCollection::AddCopy method


ينسخ نمطًا إلى هذه المجموعة.

```cpp
System::SharedPtr<Aspose::Words::Style> Aspose::Words::StyleCollection::AddCopy(const System::SharedPtr<Aspose::Words::Style> &style)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| style | const System::SharedPtr\<Aspose::Words::Style\>\& | [Style](../../style/) ليتم نسخه. |

### ReturnValue

النمط المنسوخ جاهز للاستخدام.
## ملاحظات


[Style](../../style/) to be copied can belong to the same document as well as to different document.

تم نسخ النمط المرتبط.

هذه الطريقة لا تنسخ الأنماط الأساسية.

إذا كانت المجموعة تحتوي بالفعل على نمط بالاسم نفسه، فسيتم إنشاء اسم جديد تلقائيًا بإضافة اللاحقة "_number" بدءًا من 0، مثل "Normal_0"، "Heading 1_1" وغيرها. استخدم مُعيّن [Name](../../style/get_name/) لتغيير اسم النمط المستورد.

## أمثلة



يوضح كيفية استنساخ نمط المستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// طريقة AddCopy تنشئ نسخة من النمط المحدد و
// يقوم تلقائيًا بإنشاء اسم جديد للنمط، مثل "Heading 1_0".
System::SharedPtr<Aspose::Words::Style> newStyle = doc->get_Styles()->AddCopy(doc->get_Styles()->idx_get(u"Heading 1"));

// استخدم خاصية "Name" الخاصة بالنمط لتغيير الاسم التعريفي للنمط.
newStyle->set_Name(u"My Heading 1");

// المستند الآن يحتوي على نمطين مظهرهما متطابق لكن بأسماء مختلفة.
// تغيير إعدادات أحد الأنماط لا يؤثر على الآخر.
newStyle->get_Font()->set_Color(System::Drawing::Color::get_Red());

ASSERT_EQ(u"My Heading 1", newStyle->get_Name());
ASSERT_EQ(u"Heading 1", doc->get_Styles()->idx_get(u"Heading 1")->get_Name());

ASSERT_EQ(doc->get_Styles()->idx_get(u"Heading 1")->get_Type(), newStyle->get_Type());
ASSERT_EQ(doc->get_Styles()->idx_get(u"Heading 1")->get_Font()->get_Name(), newStyle->get_Font()->get_Name());
ASPOSE_ASSERT_EQ(doc->get_Styles()->idx_get(u"Heading 1")->get_Font()->get_Size(), newStyle->get_Font()->get_Size());
ASPOSE_ASSERT_NE(doc->get_Styles()->idx_get(u"Heading 1")->get_Font()->get_Color(), newStyle->get_Font()->get_Color());
```


يوضح كيفية استيراد نمط من مستند إلى مستند مختلف.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>();

// إنشاء نمط مخصص للمستند المصدر.
System::SharedPtr<Aspose::Words::Style> srcStyle = srcDoc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");
srcStyle->get_Font()->set_Color(System::Drawing::Color::get_Red());

// استيراد النمط المخصص للمستند المصدر إلى المستند الهدف.
auto dstDoc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Style> newStyle = dstDoc->get_Styles()->AddCopy(srcStyle);

// النمط المستورد له مظهر مطابق للنمط المصدر.
ASSERT_EQ(u"MyStyle", newStyle->get_Name());
ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), newStyle->get_Font()->get_Color().ToArgb());
```

## انظر أيضًا

* Class [Style](../../style/)
* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
