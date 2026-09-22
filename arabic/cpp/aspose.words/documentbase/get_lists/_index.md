---
title: "طريقة Aspose::Words::DocumentBase::get_Lists"
linktitle: "get_Lists"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::DocumentBase::get_Lists. تُوفر الوصول إلى تنسيق القوائم المستخدم في المستند بلغة C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words/documentbase/get_lists/
---
## DocumentBase::get_Lists method


يوفر الوصول إلى تنسيق القوائم المستخدم في المستند.

```cpp
System::SharedPtr<Aspose::Words::Lists::ListCollection> Aspose::Words::DocumentBase::get_Lists() const
```

## ملاحظات


لمزيد من المعلومات، راجع وصف الفئة [ListCollection](../../../aspose.words.lists/listcollection/).

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

## انظر أيضًا

* Class [ListCollection](../../../aspose.words.lists/listcollection/)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
