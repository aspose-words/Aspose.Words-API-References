---
title: "Aspose::Words::Hyphenation class"
linktitle: "تقسيم الكلمات"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Hyphenation class. يوفر طرقًا للعمل مع قواميس التجزئة. تحدد هذه القواميس أين يمكن تجزئة الكلمات بلغة معينة. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 33000
url: /ar/cpp/aspose.words/hyphenation/
---
## Hyphenation class


يوفر طرقًا للعمل مع قواميس التجزئة. تحدد هذه القواميس أين يمكن تجزئة الكلمات في لغة معينة. لمعرفة المزيد، زر مقالة الوثائق [Working with Hyphenation](https://docs.aspose.com/words/cpp/working-with-hyphenation/)

```cpp
class Hyphenation
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| static [get_Callback](./get_callback/)() | يحصل على واجهة رد الاتصال المستخدمة لطلب القواميس عند بناء تخطيط الصفحة للمستند. يتيح ذلك تحميل القواميس بتأخير قد يكون مفيدًا عند معالجة المستندات بعدة لغات. |
| static [get_WarningCallback](./get_warningcallback/)() | يتم استدعاؤه أثناء تحميل أنماط التجزئة، عندما يتم اكتشاف مشكلة قد تؤدي إلى فقدان دقة التنسيق. |
| [Hyphenation](./hyphenation/)() |  |
| static [IsDictionaryRegistered](./isdictionaryregistered/)(const System::String\&) | يرجع **false** إذا لم يكن هناك قاموس مسجل للغة المحددة أو إذا كان القاموس المسجل Null، **true** خلاف ذلك. |
| static [RegisterDictionary](./registerdictionary/)(const System::String\&, const System::SharedPtr\<System::IO::Stream\>\&) | يسجل ويحمل قاموس تجزئة للغة المحددة من تدفق. يرمي استثناءً إذا تعذر قراءة القاموس أو كان تنسيقه غير صالح. |
| static [RegisterDictionary](./registerdictionary/)(const System::String\&, const System::String\&) | يسجل ويحمل قاموس تجزئة للغة المحددة من ملف. يرمي استثناءً إذا تعذر قراءة القاموس أو كان تنسيقه غير صالح. يمكن أيضًا استخدام هذه الطريقة لتسجيل قاموس Null لمنع [Callback](./get_callback/) من الاستدعاء المتكرر لنفس اللغة. |
| static [RegisterDictionary](./registerdictionary/)(System::String, std::basic_istream\<CharType, Traits\>\&) |  |
| static [set_Callback](./set_callback/)(const System::SharedPtr\<Aspose::Words::IHyphenationCallback\>\&) | يضبط واجهة رد الاتصال المستخدمة لطلب القواميس عند بناء تخطيط الصفحة للمستند. يتيح ذلك تحميل القواميس بتأخير قد يكون مفيدًا عند معالجة المستندات بعدة لغات. |
| static [set_WarningCallback](./set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | يتم استدعاؤه أثناء تحميل أنماط التجزئة، عندما يتم اكتشاف مشكلة قد تؤدي إلى فقدان دقة التنسيق. |
| static [UnregisterDictionary](./unregisterdictionary/)(const System::String\&) | يلغي تسجيل قاموس تجزئة للغة المحددة. هذا يختلف عن تسجيل قاموس Null. إلغاء تسجيل القاموس يتيح رد الاتصال للغة المحددة. |
## انظر أيضًا

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
