---
title: "طريقة Aspose::Words::CleanupOptions::get_UnusedBuiltinStyles"
linktitle: "get_UnusedBuiltinStyles"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::CleanupOptions::get_UnusedBuiltinStyles. يحدد أن الأنماط المدمجة غير المستخدمة يجب إزالتها من المستند في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words/cleanupoptions/get_unusedbuiltinstyles/
---
## CleanupOptions::get_UnusedBuiltinStyles method


يحدد أن الأنماط [BuiltIn](../../style/get_builtin/) غير المستخدمة يجب إزالتها من المستند.

```cpp
bool Aspose::Words::CleanupOptions::get_UnusedBuiltinStyles() const
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

* Class [CleanupOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
