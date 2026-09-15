---
title: "فئة Aspose::Words::CleanupOptions"
linktitle: "CleanupOptions"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::CleanupOptions. تسمح بتحديد خيارات تنظيف المستند. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 10000
url: /ar/cpp/aspose.words/cleanupoptions/
---
## CleanupOptions class


يسمح بتحديد خيارات تنظيف المستند. لمعرفة المزيد، زر مقالة الوثائق [Clean Up a Document](https://docs.aspose.com/words/cpp/clean-up-a-document/).

```cpp
class CleanupOptions : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [CleanupOptions](./cleanupoptions/)() |  |
| [get_DuplicateStyle](./get_duplicatestyle/)() const | يحصل/يضبط علامة تشير إلى ما إذا كان يجب إزالة الأنماط المكررة من المستند. القيمة الافتراضية هي **false**. |
| [get_UnusedBuiltinStyles](./get_unusedbuiltinstyles/)() const | يحدد أن الأنماط غير المستخدمة [BuiltIn](../style/get_builtin/) يجب إزالتها من المستند. |
| [get_UnusedLists](./get_unusedlists/)() const | يحدد ما إذا كان يجب إزالة القوائم غير المستخدمة وتعريفات القوائم من المستند. القيمة الافتراضية هي **true**. |
| [get_UnusedStyles](./get_unusedstyles/)() const | يحدد ما إذا كان يجب إزالة الأنماط غير المستخدمة من المستند. القيمة الافتراضية هي **true**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_DuplicateStyle](./set_duplicatestyle/)(bool) | المحدد لـ [Aspose::Words::CleanupOptions::get_DuplicateStyle](./get_duplicatestyle/). |
| [set_UnusedBuiltinStyles](./set_unusedbuiltinstyles/)(bool) | المحدد لـ [Aspose::Words::CleanupOptions::get_UnusedBuiltinStyles](./get_unusedbuiltinstyles/). |
| [set_UnusedLists](./set_unusedlists/)(bool) | المحدد لـ [Aspose::Words::CleanupOptions::get_UnusedLists](./get_unusedlists/). |
| [set_UnusedStyles](./set_unusedstyles/)(bool) | المحدد لـ [Aspose::Words::CleanupOptions::get_UnusedStyles](./get_unusedstyles/). |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
