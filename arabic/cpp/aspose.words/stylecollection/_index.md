---
title: "فئة Aspose::Words::StyleCollection"
linktitle: "StyleCollection"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::StyleCollection. مجموعة من كائنات Style التي تمثل الأنماط المدمجة والمحددة من قبل المستخدم في المستند. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 65000
url: /ar/cpp/aspose.words/stylecollection/
---
## StyleCollection class


مجموعة من كائنات [Style](../style/) التي تمثل الأنماط المدمجة والمحددة من قبل المستخدم في المستند. لمعرفة المزيد، زر مقالة الوثائق [Working with Styles and Themes](https://docs.aspose.com/words/cpp/working-with-styles-and-themes/).

```cpp
class StyleCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Style>>
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [Add](./add/)(Aspose::Words::StyleType, const System::String\&) | ينشئ نمطًا جديدًا معرفًا من قبل المستخدم ويضيفه إلى المجموعة. |
| [AddCopy](./addcopy/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | ينسخ نمطًا إلى هذه المجموعة. |
| [ClearQuickStyleGallery](./clearquickstylegallery/)() | يزيل جميع الأنماط من لوحة معرض Quick [Style](../style/). |
| [get_Count](./get_count/)() | يحصل على عدد الأنماط في المجموعة. |
| [get_DefaultFont](./get_defaultfont/)() | يحصل على تنسيق النص الافتراضي للمستند. |
| [get_DefaultParagraphFormat](./get_defaultparagraphformat/)() | يحصل على تنسيق الفقرة الافتراضي للمستند. |
| [get_Document](./get_document/)() const | يحصل على المستند المالِك. |
| [GetEnumerator](./getenumerator/)() override | يحصل على كائن عداد سيعد الأنماط بترتيب أبجدي حسب أسمائها. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(const System::String\&) | يحصل على نمط بالاسم أو الاسم المستعار. |
| [idx_get](./idx_get/)(Aspose::Words::StyleIdentifier) | يحصل على نمط مدمج بواسطة معرفه المستقل عن اللغة. |
| [idx_get](./idx_get/)(int32_t) | يحصل على نمط حسب الفهرس. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## أمثلة



يظهر كيفية إنشاء واستخدام نمط فقرة مع تنسيق القائمة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// إنشاء نمط فقرة مخصص.
System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle1");
style->get_Font()->set_Size(24);
style->get_Font()->set_Name(u"Verdana");
style->get_ParagraphFormat()->set_SpaceAfter(12);

// إنشاء قائمة والتأكد من أن الفقرات التي تستخدم هذا النمط ستستخدم هذه القائمة.
style->get_ListFormat()->set_List(doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::BulletDefault));
style->get_ListFormat()->set_ListLevelNumber(0);

// تطبيق نمط الفقرة على الفقرة الحالية لمُنشئ المستند، ثم إضافة بعض النص.
builder->get_ParagraphFormat()->set_Style(style);
builder->Writeln(u"Hello World: MyStyle1, bulleted list.");

// غيّر نمط مُنشئ المستند إلى نمط لا يحتوي على تنسيق القوائم واكتب فقرة أخرى.
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Normal"));
builder->Writeln(u"Hello World: Normal.");

builder->get_Document()->Save(get_ArtifactsDir() + u"Styles.ParagraphStyleBulletedList.docx");
```

## انظر أيضًا

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
