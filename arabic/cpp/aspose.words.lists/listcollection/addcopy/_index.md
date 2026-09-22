---
title: "طريقة Aspose::Words::Lists::ListCollection::AddCopy"
linktitle: "AddCopy"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Lists::ListCollection::AddCopy. تنشئ قائمة جديدة عن طريق نسخ القائمة المحددة وإضافتها إلى مجموعة القوائم في المستند في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.lists/listcollection/addcopy/
---
## ListCollection::AddCopy method


ينشئ قائمة جديدة عن طريق نسخ القائمة المحددة وإضافتها إلى مجموعة القوائم في المستند.

```cpp
System::SharedPtr<Aspose::Words::Lists::List> Aspose::Words::Lists::ListCollection::AddCopy(const System::SharedPtr<Aspose::Words::Lists::List> &srcList)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| srcList | const System::SharedPtr\<Aspose::Words::Lists::List\>\& | القائمة المصدر للنسخ منها. |

### ReturnValue

القائمة التي تم إنشاؤها حديثًا.
## ملاحظات


يمكن أن تكون القائمة المصدر من أي مستند. إذا كانت القائمة المصدر تنتمي إلى مستند مختلف، يتم إنشاء نسخة من القائمة وإضافتها إلى المستند الحالي.

إذا كانت القائمة المصدر إشارة إلى أو تعريف لنمط قائمة، فإن القائمة التي تم إنشاؤها حديثًا لا ترتبط بنمط القائمة الأصلي.

## أمثلة



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

* Class [List](../../list/)
* Class [ListCollection](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
