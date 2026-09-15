---
title: "Aspose::Words::Lists::ListCollection class"
linktitle: "ListCollection"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Lists::ListCollection class. يخزن ويدير تنسيق القوائم النقطية والمرقمة المستخدمة في المستند. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.lists/listcollection/
---
## ListCollection class


يخزن ويدير تنسيق القوائم النقطية والمرقمة المستخدمة في مستند. لمعرفة المزيد، زر مقالة الوثائق [Working with Lists](https://docs.aspose.com/words/cpp/working-with-lists/).

```cpp
class ListCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Lists::List>>
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [Add](./add/)(Aspose::Words::Lists::ListTemplate) | ينشئ قائمة جديدة بناءً على قالب محدد مسبقًا ويضيفها إلى مجموعة القوائم في المستند. |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | ينشئ قائمة جديدة تشير إلى نمط قائمة ويضيفها إلى مجموعة القوائم في المستند. |
| [AddCopy](./addcopy/)(const System::SharedPtr\<Aspose::Words::Lists::List\>\&) | ينشئ قائمة جديدة عن طريق نسخ القائمة المحددة وإضافتها إلى مجموعة القوائم في المستند. |
| [AddSingleLevelList](./addsinglelevellist/)(Aspose::Words::Lists::ListTemplate) | ينشئ قائمة ذات مستوى واحد جديدة بناءً على القالب المحدد مسبقًا ويضيفها إلى مجموعة القوائم في المستند. |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | يحصل على عدد القوائم المرقمة والنقطية في المستند. |
| [get_Document](./get_document/)() const | يحصل على المستند المالِك. |
| [GetEnumerator](./getenumerator/)() override | يحصل على كائن المُعدِّد الذي سيعد القوائم في المستند. |
| [GetListByListId](./getlistbylistid/)(int32_t) | يحصل على قائمة باستخدام معرف القائمة. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | يحصل على قائمة بواسطة الفهرس. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
## Typedefs

| تعريف نوع | الوصف |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |
## ملاحظات


القائمة في مستند Microsoft Word هي مجموعة من خصائص تنسيق القوائم. يتم تخزين تنسيق القوائم في مجموعة [ListCollection](./) بشكل منفصل عن فقرات النص.

أنت لا تنشئ كائنات من هذه الفئة. هناك دائمًا كائن واحد فقط من نوع [ListCollection](./) لكل مستند ويمكن الوصول إليه عبر الخاصية [Lists](../../aspose.words/documentbase/get_lists/).

لإنشاء قائمة جديدة بناءً على قالب قائمة محدد مسبقًا أو بناءً على نمط قائمة، استخدم الطريقة [Add()](../).

لإنشاء قائمة جديدة بتنسيق مطابق لقائمة موجودة، استخدم الطريقة [AddCopy()](../).

لجعل فقرة ذات تعداد نقطي أو رقمي، تحتاج إلى تطبيق تنسيق القائمة على الفقرة عن طريق تعيين كائن [List](../list/) إلى الخاصية [List](../listformat/get_list/) في [ListFormat](../listformat/).

لإزالة تنسيق القائمة من فقرة، استخدم الطريقة [RemoveNumbers](../listformat/removenumbers/).

إذا كنت تعرف قليلًا عن WordprocessingML، فقد تعرف أنه يعرّف مفاهيم منفصلة لـ "list" و "list definition". وهذا يتطابق تمامًا مع طريقة تخزين تنسيق القوائم في مستند Microsoft Word على المستوى المنخفض. تعريف [List](../list/) يشبه "المخطط" والقائمة تشبه نسخة من تعريف القائمة.

لتبسيط نموذج البرمجة، تقوم Aspose.Words بإخفاء التمييز بين القائمة وتعريف القائمة بنفس الطريقة التي يخفي بها Microsoft Word ذلك في واجهة المستخدم. هذا يسمح لك بالتركيز أكثر على الشكل الذي تريد أن يبدو عليه المستند، بدلاً من بناء كائنات منخفضة المستوى لتلبية متطلبات تنسيق ملف Microsoft Word.

ليس من الممكن حذف القوائم بمجرد إنشائها في الإصدار الحالي من [Aspose.Words](../../aspose.words/). هذا مشابه لـ Microsoft Word حيث لا يمتلك المستخدم سيطرة صريحة على تعريفات القوائم.

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
