---
title: "طريقة Aspose::Words::Document::Cleanup"
linktitle: "Cleanup"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Document::Cleanup. تنظف الأنماط والقوائم غير المستخدمة من المستند في C++."
type: docs
weight: 6000
url: /ar/cpp/aspose.words/document/cleanup/
---
## Document::Cleanup() method


ينظف الأنماط والقوائم غير المستخدمة من المستند.

```cpp
void Aspose::Words::Document::Cleanup()
```


## أمثلة



يوضح كيفية إزالة الأنماط المخصصة غير المستخدمة من المستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

doc->get_Styles()->Add(Aspose::Words::StyleType::List, u"MyListStyle1");
doc->get_Styles()->Add(Aspose::Words::StyleType::List, u"MyListStyle2");
doc->get_Styles()->Add(Aspose::Words::StyleType::Character, u"MyParagraphStyle1");
doc->get_Styles()->Add(Aspose::Words::StyleType::Character, u"MyParagraphStyle2");

// مع الأنماط المدمجة، يحتوي المستند الآن على ثمانية أنماط.
// يُعتبر النمط المخصص "مستخدمًا" عندما يُطبق على جزء من المستند،
// مما يعني أن الأنماط الأربعة التي أضفناها غير مستخدمة حاليًا.
ASSERT_EQ(8, doc->get_Styles()->get_Count());

// طبق نمط حرف مخصص، ثم نمط قائمة مخصص. سيتسبب ذلك في تعليم الأنماط كـ "مستخدمة".
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->get_Font()->set_Style(doc->get_Styles()->idx_get(u"MyParagraphStyle1"));
builder->Writeln(u"Hello world!");

System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->Add(doc->get_Styles()->idx_get(u"MyListStyle1"));
builder->get_ListFormat()->set_List(list);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");

doc->Cleanup();

ASSERT_EQ(6, doc->get_Styles()->get_Count());

// إزالة كل عقدة يُطبق عليها نمط مخصص يضع علامة "غير مستخدم" عليها مرة أخرى.
// شغّل طريقة Cleanup مرة أخرى لإزالتها.
doc->get_FirstSection()->get_Body()->RemoveAllChildren();
doc->Cleanup();

ASSERT_EQ(4, doc->get_Styles()->get_Count());
```

## انظر أيضًا

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Cleanup(const System::SharedPtr\<Aspose::Words::CleanupOptions\>\&) method


تنظف الأنماط والقوائم غير المستخدمة من المستند بناءً على [CleanupOptions](../../cleanupoptions/) المحددة.

```cpp
void Aspose::Words::Document::Cleanup(const System::SharedPtr<Aspose::Words::CleanupOptions> &options)
```


## أمثلة



يوضح كيفية إزالة جميع الأنماط المخصصة غير المستخدمة من المستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

doc->get_Styles()->Add(Aspose::Words::StyleType::List, u"MyListStyle1");
doc->get_Styles()->Add(Aspose::Words::StyleType::List, u"MyListStyle2");
doc->get_Styles()->Add(Aspose::Words::StyleType::Character, u"MyParagraphStyle1");
doc->get_Styles()->Add(Aspose::Words::StyleType::Character, u"MyParagraphStyle2");

// مع الأنماط المدمجة، يحتوي المستند الآن على ثمانية أنماط.
// يتم وضع علامة "مستخدم" على النمط المخصص طالما هناك أي نص داخل المستند
// مُنسق بذلك النمط. هذا يعني أن الأنماط الأربعة التي أضفناها غير مستخدمة حاليًا.
ASSERT_EQ(8, doc->get_Styles()->get_Count());

// طبق نمط حرف مخصص، ثم نمط قائمة مخصص. سيؤدي ذلك إلى وضع علامة "مستخدم" عليها.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->get_Font()->set_Style(doc->get_Styles()->idx_get(u"MyParagraphStyle1"));
builder->Writeln(u"Hello world!");

System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->Add(doc->get_Styles()->idx_get(u"MyListStyle1"));
builder->get_ListFormat()->set_List(list);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");

// الآن، هناك نمط حرف غير مستخدم واحد ونمط قائمة غير مستخدم واحد.
// طريقة Cleanup()، عند تكوينها باستخدام كائن CleanupOptions، يمكنها استهداف الأنماط غير المستخدمة وإزالتها.
auto cleanupOptions = System::MakeObject<Aspose::Words::CleanupOptions>();
cleanupOptions->set_UnusedLists(true);
cleanupOptions->set_UnusedStyles(true);
cleanupOptions->set_UnusedBuiltinStyles(true);

doc->Cleanup(cleanupOptions);

ASSERT_EQ(4, doc->get_Styles()->get_Count());

// إزالة كل عقدة يُطبق عليها نمط مخصص يضع علامة "غير مستخدم" عليها مرة أخرى.
// أعد تشغيل طريقة Cleanup لإزالتها.
doc->get_FirstSection()->get_Body()->RemoveAllChildren();
doc->Cleanup(cleanupOptions);

ASSERT_EQ(2, doc->get_Styles()->get_Count());
```

## انظر أيضًا

* Class [CleanupOptions](../../cleanupoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
