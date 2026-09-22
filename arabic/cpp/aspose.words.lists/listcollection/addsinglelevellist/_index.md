---
title: "Aspose::Words::Lists::ListCollection::AddSingleLevelList طريقة"
linktitle: "AddSingleLevelList"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Lists::ListCollection::AddSingleLevelList طريقة. ينشئ قائمة ذات مستوى واحد جديدة بناءً على القالب المحدد مسبقًا ويضيفها إلى مجموعة القوائم في المستند في C++."
type: docs
weight: 3500
url: /ar/cpp/aspose.words.lists/listcollection/addsinglelevellist/
---
## ListCollection::AddSingleLevelList method


ينشئ قائمة ذات مستوى واحد جديدة بناءً على القالب المحدد مسبقًا ويضيفها إلى مجموعة القوائم في المستند.

```cpp
System::SharedPtr<Aspose::Words::Lists::List> Aspose::Words::Lists::ListCollection::AddSingleLevelList(Aspose::Words::Lists::ListTemplate listTemplate)
```


## أمثلة



يوضح كيفية إنشاء قائمة ذات مستوى واحد جديدة بناءً على القالب المحدد مسبقًا.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Lists::ListCollection> listCollection = doc->get_Lists();

// ينشئ القائمة النقطية من قالب BulletCircle.
System::SharedPtr<Aspose::Words::Lists::List> bulletedList = listCollection->AddSingleLevelList(Aspose::Words::Lists::ListTemplate::BulletCircle);

// يكتب القائمة النقطية إلى المستند الناتج.
builder->Writeln(u"Bulleted list starts below:");
builder->get_ListFormat()->set_List(bulletedList);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");
builder->get_ListFormat()->RemoveNumbers();

// ينشئ القائمة المرقمة من قالب NumberUppercaseLetterDot.
System::SharedPtr<Aspose::Words::Lists::List> numberedList = listCollection->AddSingleLevelList(Aspose::Words::Lists::ListTemplate::NumberUppercaseLetterDot);

// يكتب القائمة المرقمة إلى المستند الناتج.
builder->Writeln(u"Numbered list starts below:");
builder->get_ListFormat()->set_List(numberedList);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");

doc->Save(get_ArtifactsDir() + u"Lists.AddSingleLevelList.docx");
```

## انظر أيضًا

* Class [List](../../list/)
* Enum [ListTemplate](../../listtemplate/)
* Class [ListCollection](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
