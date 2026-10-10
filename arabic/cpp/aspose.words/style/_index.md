---
title: "فئة Aspose::Words::Style"
linktitle: "نمط"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::Style. تمثل نمطًا مدمجًا أو معرفًا من قبل المستخدم. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 64000
url: /ar/cpp/aspose.words/style/
---
## Style class


يمثل نمطًا مدمجًا أو معرفًا من قبل المستخدم. لمعرفة المزيد، زر مقالة الوثائق [Working with Styles and Themes](https://docs.aspose.com/words/cpp/working-with-styles-and-themes/).

```cpp
class Style : public Aspose::Words::IParaAttrSource,
              public Aspose::Words::IRunAttrSource
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | يقارن بالنمط المحدد. يتم مقارنة معرفات الأنماط للأنماط المدمجة فقط. لا تُضمّن القيم الافتراضية للأنماط في المقارنة. يتم مقارنة النمط الأساسي، والنمط المرتبط، ونمط الفقرة التالية بشكل متكرر. |
| [get_Aliases](./get_aliases/)() | يحصل على جميع الأسماء المستعارة لهذا النمط. إذا لم يكن للنمط أي أسماء مستعارة فسيتم إرجاع مصفوفة فارغة من السلاسل. |
| [get_AutomaticallyUpdate](./get_automaticallyupdate/)() const | يحدد ما إذا كان هذا النمط يُعاد تعريفه تلقائيًا بناءً على القيمة المناسبة. |
| [get_BaseStyleName](./get_basestylename/)() | يحصل/يضبط اسم النمط الذي يُبنى عليه هذا النمط. |
| [get_BuiltIn](./get_builtin/)() | صحيح إذا كان هذا النمط أحد الأنماط المدمجة في MS Word. |
| [get_Document](./get_document/)() | يحصل على المستند المالِك. |
| [get_Font](./get_font/)() | يحصل على تنسيق الأحرف للنمط. |
| [get_IsHeading](./get_isheading/)() | صحيح عندما يكون النمط أحد أنماط العناوين المدمجة. |
| [get_IsQuickStyle](./get_isquickstyle/)() const | يحدد ما إذا كان هذا النمط معروضًا في معرض [Style](./) السريع داخل واجهة مستخدم MS Word. |
| [get_LinkedStyleName](./get_linkedstylename/)() | يحصل/يضبط اسم الـ[Style](./) المرتبط بهذا. يُرجع سلسلة فارغة إذا لم يكن هناك أنماط مرتبطة. |
| [get_List](./get_list/)() | يحصل على القائمة التي تحدد تنسيق نمط القائمة هذا. |
| [get_ListFormat](./get_listformat/)() | يوفر الوصول إلى خصائص تنسيق القائمة لنمط الفقرة. |
| [get_Locked](./get_locked/)() const | يحدد ما إذا كان هذا النمط مقفلًا. |
| [get_Name](./get_name/)() const | يحصل أو يضبط اسم النمط. |
| [get_NextParagraphStyleName](./get_nextparagraphstylename/)() | يحصل/يضبط اسم النمط الذي يُطبق تلقائيًا على فقرة جديدة تُدرج بعد فقرة مُنسقة بالنمط المحدد. |
| [get_ParagraphFormat](./get_paragraphformat/)() | يحصل على تنسيق الفقرة للنمط. |
| [get_Priority](./get_priority/)() const | يحصل/يضبط القيمة الصحيحة التي تمثل الأولوية لفرز الأنماط في لوحة مهام الأنماط. |
| [get_SemiHidden](./get_semihidden/)() const | يحصل/يضبط ما إذا كان النمط يختفي من معرض الأنماط ومن لوحة مهام الأنماط. |
| [get_StyleIdentifier](./get_styleidentifier/)() const | يحصل على معرف النمط المستقل عن اللغة لنمط مدمج. |
| [get_Styles](./get_styles/)() const | يحصل على مجموعة الأنماط التي ينتمي إليها هذا النمط. |
| [get_Type](./get_type/)() const | يحصل على نوع النمط (فقرة أو حرف). |
| [get_UnhideWhenUsed](./get_unhidewhenused/)() const | يحصل/يضبط ما إذا كان النمط المستخدم في المستند الحالي يُظهر نفسه مرة أخرى في معرض الأنماط ومن لوحة مهام الأنماط. يكون صحيحًا عندما يجب إظهار النمط المستخدم في معرض الأنماط. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() | يزيل النمط المحدد من المستند. |
| [set_AutomaticallyUpdate](./set_automaticallyupdate/)(bool) | محدد لـ [Aspose::Words::Style::get_AutomaticallyUpdate](./get_automaticallyupdate/). |
| [set_BaseStyleName](./set_basestylename/)(const System::String\&) | محدد لـ [Aspose::Words::Style::get_BaseStyleName](./get_basestylename/). |
| [set_IsQuickStyle](./set_isquickstyle/)(bool) | محدد لـ [Aspose::Words::Style::get_IsQuickStyle](./get_isquickstyle/). |
| [set_LinkedStyleName](./set_linkedstylename/)(const System::String\&) | محدد لـ [Aspose::Words::Style::get_LinkedStyleName](./get_linkedstylename/). |
| [set_Locked](./set_locked/)(bool) | محدد لـ [Aspose::Words::Style::get_Locked](./get_locked/). |
| [set_Name](./set_name/)(const System::String\&) | محدد لـ [Aspose::Words::Style::get_Name](./get_name/). |
| [set_NextParagraphStyleName](./set_nextparagraphstylename/)(const System::String\&) | محدد لـ [Aspose::Words::Style::get_NextParagraphStyleName](./get_nextparagraphstylename/). |
| [set_Priority](./set_priority/)(int32_t) | محدد لـ [Aspose::Words::Style::get_Priority](./get_priority/). |
| [set_SemiHidden](./set_semihidden/)(bool) | محدد لـ [Aspose::Words::Style::get_SemiHidden](./get_semihidden/). |
| [set_UnhideWhenUsed](./set_unhidewhenused/)(bool) | محدد لـ [Aspose::Words::Style::get_UnhideWhenUsed](./get_unhidewhenused/). |
| static [Type](./type/)() |  |

## أمثلة



يظهر كيفية إنشاء وتطبيق نمط مخصص.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");
style->get_Font()->set_Name(u"Times New Roman");
style->get_Font()->set_Size(16);
style->get_Font()->set_Color(System::Drawing::Color::get_Navy());
// إعادة تعريف النمط تلقائيًا.
style->set_AutomaticallyUpdate(true);

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// تطبيق أحد الأنماط من المستند على الفقرة التي ينشئها مُنشئ المستند.
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"MyStyle"));
builder->Writeln(u"Hello world!");

System::SharedPtr<Aspose::Words::Style> firstParagraphStyle = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Style();

ASPOSE_ASSERT_EQ(style, firstParagraphStyle);

// إزالة نمطنا المخصص من مجموعة أنماط المستند.
doc->get_Styles()->idx_get(u"MyStyle")->Remove();

firstParagraphStyle = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Style();

// أي نص كان يستخدم نمطًا مُزالًا يعود إلى التنسيق الافتراضي.
ASSERT_FALSE(doc->get_Styles()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Style>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Style> s)>>([](System::SharedPtr<Aspose::Words::Style> s) -> bool
{
    return s->get_Name() == u"MyStyle";
}))));
ASSERT_EQ(u"Times New Roman", firstParagraphStyle->get_Font()->get_Name());
ASPOSE_ASSERT_EQ(12.0, firstParagraphStyle->get_Font()->get_Size());
ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), firstParagraphStyle->get_Font()->get_Color().ToArgb());
```


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
