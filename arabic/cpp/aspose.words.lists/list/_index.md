---
title: "Aspose::Words::Lists::List class"
linktitle: "List"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Lists::List class. يمثل تنسيق قائمة. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 1000
url: /ar/cpp/aspose.words.lists/list/
---
## List class


يمثل تنسيق قائمة. لمعرفة المزيد، زر مقالة الوثائق [Working with Lists](https://docs.aspose.com/words/cpp/working-with-lists/).

```cpp
class List : public System::IComparable<System::SharedPtr<Aspose::Words::Lists::List>>
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [CompareTo](./compareto/)(System::SharedPtr\<Aspose::Words::Lists::List\>) override | يقارن القائمة المحددة بالقائمة الحالية. |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::Lists::List\>\&) | يقارن بالقائمة المحددة. |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | يحدد ما إذا كان الكائن المحدد مساوٍ في القيمة للكائن الحالي. |
| [get_Document](./get_document/)() const | يحصل على المستند المالِك. |
| [get_IsListStyleDefinition](./get_isliststyledefinition/)() | يرجع **true** إذا كانت هذه القائمة تعريفًا لنمط قائمة. |
| [get_IsListStyleReference](./get_isliststylereference/)() | يرجع **true** إذا كانت هذه القائمة إشارة إلى نمط قائمة. |
| [get_IsMultiLevel](./get_ismultilevel/)() | يرجع **true** عندما تحتوي القائمة على 9 مستويات؛ **false** عندما تكون مستوى واحد. |
| [get_IsRestartAtEachSection](./get_isrestartateachsection/)() | يحدد ما إذا كان يجب إعادة بدء القائمة في كل قسم. القيمة الافتراضية هي **false**. |
| [get_ListId](./get_listid/)() const | يحصل على المعرف الفريد للقائمة. |
| [get_ListLevels](./get_listlevels/)() | يحصل على مجموعة مستويات القائمة لهذه القائمة. |
| [get_Style](./get_style/)() | يحصل على نمط القائمة الذي تشير إليه هذه القائمة أو تعرفه. |
| [GetHashCode](./gethashcode/)() const override | يحسب قيمة التجزئة لهذا كائن القائمة. |
| [GetType](./gettype/)() const override |  |
| [HasSameTemplate](./hassametemplate/)(const System::SharedPtr\<Aspose::Words::Lists::List\>\&) | يرجع true إذا تم إنشاء القائمة الحالية والقائمة المعطاة من نفس القالب. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_IsRestartAtEachSection](./set_isrestartateachsection/)(bool) | المحدد لـ [Aspose::Words::Lists::List::get_IsRestartAtEachSection](./get_isrestartateachsection/). |
| static [Type](./type/)() |  |
## ملاحظات


القائمة في مستند Microsoft Word هي مجموعة من خصائص تنسيق القوائم. يمكن لكل قائمة أن تحتوي على ما يصل إلى 9 مستويات وخصائص تنسيق، مثل نمط الرقم، قيمة البداية، المسافة البادئة، موضع علامة التبويب، إلخ، يتم تعريفها بشكل منفصل لكل مستوى.

كائن [List](./) ينتمي دائمًا إلى مجموعة [ListCollection](../listcollection/).

لإنشاء قائمة جديدة، استخدم طرق Add في مجموعة [ListCollection](../listcollection/).

لتعديل تنسيق قائمة، استخدم كائنات [ListLevel](../listlevel/) الموجودة في مجموعة [ListLevels](./get_listlevels/).

لتطبيق أو إزالة تنسيق القائمة من فقرة، استخدم [ListFormat](../listformat/).

## أمثلة



يعرض كيفية العمل مع مستويات القوائم.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

ASSERT_FALSE(builder->get_ListFormat()->get_IsListItem());

// تتيح لنا القائمة تنظيم وتزيين مجموعات الفقرات باستخدام رموز البادئة والمسافات البادئة.
// يمكننا إنشاء قوائم متداخلة بزيادة مستوى المسافة البادئة.
// يمكننا بدء وإنهاء قائمة باستخدام خاصية "ListFormat" لكائن Document Builder.
// كل فقرة نضيفها بين بداية القائمة ونهايتها ستصبح عنصرًا في القائمة.
// فيما يلي نوعان من القوائم يمكننا إنشاؤهما باستخدام Document Builder.
// 1 -  قائمة مرقمة:
// القوائم المرقمة تُنشئ ترتيبًا منطقيًا للفقرات عن طريق ترقيم كل عنصر.
builder->get_ListFormat()->set_List(doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault));

ASSERT_TRUE(builder->get_ListFormat()->get_IsListItem());

// عن طريق ضبط الخاصية "ListLevelNumber"، يمكننا زيادة مستوى القائمة
// لبدء قائمة فرعية مستقلة عند عنصر القائمة الحالي.
// قالب القائمة في Microsoft Word المسمى "NumberDefault" يستخدم الأرقام لإنشاء مستويات القائمة للمستوى الأول.
// المستويات الأعمق للقائمة تستخدم الأحرف والأرقام الرومانية الصغيرة.
for (int32_t i = 0; i < 9; i++)
{
    builder->get_ListFormat()->set_ListLevelNumber(i);
    builder->Writeln(System::String(u"Level ") + i);
}

// 2 -  قائمة نقطية:
// ستُطبق هذه القائمة مسافة بادئة ورمز نقطي ("•") قبل كل فقرة.
// المستويات الأعمق لهذه القائمة ستستخدم رموزًا مختلفة، مثل "■" و "○".
builder->get_ListFormat()->set_List(doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::BulletDefault));

for (int32_t i = 0; i < 9; i++)
{
    builder->get_ListFormat()->set_ListLevelNumber(i);
    builder->Writeln(System::String(u"Level ") + i);
}

// يمكننا تعطيل تنسيق القوائم لتجنب تنسيق أي فقرات لاحقة كقوائم عن طريق إلغاء تعيين علامة "List".
builder->get_ListFormat()->set_List(nullptr);

ASSERT_FALSE(builder->get_ListFormat()->get_IsListItem());

doc->Save(get_ArtifactsDir() + u"Lists.SpecifyListLevel.docx");
```


يوضح كيفية تطبيق تنسيق قائمة مخصص على الفقرات عند استخدام [DocumentBuilder](../../aspose.words/documentbuilder/).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// تتيح لنا القائمة تنظيم وتزيين مجموعات الفقرات باستخدام رموز البادئة والمسافات البادئة.
// يمكننا إنشاء قوائم متداخلة بزيادة مستوى المسافة البادئة.
// يمكننا بدء وإنهاء قائمة باستخدام خاصية "ListFormat" لكائن Document Builder.
// كل فقرة نضيفها بين بداية القائمة ونهايتها ستصبح عنصرًا في القائمة.
// إنشاء قائمة من قالب Microsoft Word، وتخصيص أول مستويين من مستوياتها.
System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault);

System::SharedPtr<Aspose::Words::Lists::ListLevel> listLevel = list->get_ListLevels()->idx_get(0);
listLevel->get_Font()->set_Color(System::Drawing::Color::get_Red());
listLevel->get_Font()->set_Size(24);
listLevel->set_NumberStyle(Aspose::Words::NumberStyle::OrdinalText);
listLevel->set_StartAt(21);
listLevel->set_NumberFormat(u"\x0000");

listLevel->set_NumberPosition(-36);
listLevel->set_TextPosition(144);
listLevel->set_TabPosition(144);

listLevel = list->get_ListLevels()->idx_get(1);
listLevel->set_Alignment(Aspose::Words::Lists::ListLevelAlignment::Right);
listLevel->set_NumberStyle(Aspose::Words::NumberStyle::Bullet);
listLevel->get_Font()->set_Name(u"Wingdings");
listLevel->get_Font()->set_Color(System::Drawing::Color::get_Blue());
listLevel->get_Font()->set_Size(24);

// ستُنشئ قيمة NumberFormat هذه رموز تعداد نقطية على شكل نجمة.
listLevel->set_NumberFormat(u"\xf0af");
listLevel->set_TrailingCharacter(Aspose::Words::Lists::ListTrailingCharacter::Space);
listLevel->set_NumberPosition(144);

// إنشاء فقرات وتطبيق كلا مستويي القائمة من تنسيقنا المخصص علىها.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ListFormat()->set_List(list);
builder->Writeln(u"The quick brown fox...");
builder->Writeln(u"The quick brown fox...");

builder->get_ListFormat()->ListIndent();
builder->Writeln(u"jumped over the lazy dog.");
builder->Writeln(u"jumped over the lazy dog.");

builder->get_ListFormat()->ListOutdent();
builder->Writeln(u"The quick brown fox...");

builder->get_ListFormat()->RemoveNumbers();

builder->get_Document()->Save(get_ArtifactsDir() + u"Lists.CreateCustomList.docx");
```


يظهر كيفية إعادة بدء الترقيم في قائمة عن طريق نسخ القائمة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// تتيح لنا القائمة تنظيم وتزيين مجموعات الفقرات باستخدام رموز البادئة والمسافات البادئة.
// يمكننا إنشاء قوائم متداخلة بزيادة مستوى المسافة البادئة.
// يمكننا بدء وإنهاء قائمة باستخدام خاصية "ListFormat" لكائن Document Builder.
// كل فقرة نضيفها بين بداية القائمة ونهايتها ستصبح عنصرًا في القائمة.
// أنشئ قائمة من قالب Microsoft Word، وقم بتخصيص المستوى الأول للقائمة.
System::SharedPtr<Aspose::Words::Lists::List> list1 = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberArabicParenthesis);
list1->get_ListLevels()->idx_get(0)->get_Font()->set_Color(System::Drawing::Color::get_Red());
list1->get_ListLevels()->idx_get(0)->set_Alignment(Aspose::Words::Lists::ListLevelAlignment::Right);

// طبق قائمتنا على بعض الفقرات.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"List 1 starts below:");
builder->get_ListFormat()->set_List(list1);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");
builder->get_ListFormat()->RemoveNumbers();

// يمكننا إضافة نسخة من قائمة موجودة إلى مجموعة قوائم المستند
// لإنشاء قائمة مشابهة دون تعديل الأصل.
System::SharedPtr<Aspose::Words::Lists::List> list2 = doc->get_Lists()->AddCopy(list1);
list2->get_ListLevels()->idx_get(0)->get_Font()->set_Color(System::Drawing::Color::get_Blue());
list2->get_ListLevels()->idx_get(0)->set_StartAt(10);

// طبق القائمة الثانية على فقرات جديدة.
builder->Writeln(u"List 2 starts below:");
builder->get_ListFormat()->set_List(list2);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");
builder->get_ListFormat()->RemoveNumbers();

doc->Save(get_ArtifactsDir() + u"Lists.RestartNumberingUsingListCopy.docx");
```

## انظر أيضًا

* Namespace [Aspose::Words::Lists](../)
* Library [Aspose.Words for C++](../../)
