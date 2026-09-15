---
title: "طريقة Aspose::Words::Lists::ListLevel::get_NumberPosition"
linktitle: "get_NumberPosition"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Lists::ListLevel::get_NumberPosition. يرجع أو يضبط الموضع (بالنقاط) للرقم أو الرصاصة لمستوى القائمة في C++."
type: docs
weight: 13000
url: /ar/cpp/aspose.words.lists/listlevel/get_numberposition/
---
## ListLevel::get_NumberPosition method


يعيد أو يضبط موضع (بالنقاط) الرقم أو الرصاصة للمستوى من القائمة.

```cpp
double Aspose::Words::Lists::ListLevel::get_NumberPosition() const
```

## ملاحظات


[NumberPosition](./) corresponds to LeftIndent plus FirstLineIndent of the paragraph.

## أمثلة



يوضح كيفية تطبيق تنسيق قائمة مخصص على الفقرات عند استخدام [DocumentBuilder](../../../aspose.words/documentbuilder/).
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

## انظر أيضًا

* Class [ListLevel](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
