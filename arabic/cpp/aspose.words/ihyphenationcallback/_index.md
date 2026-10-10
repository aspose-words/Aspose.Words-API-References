---
title: "Aspose::Words::IHyphenationCallback interface"
linktitle: "IHyphenationCallback"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "واجهة Aspose::Words::IHyphenationCallback. يتم تنفيذها بواسطة الفئات التي يمكنها تسجيل قواميس التجزئة في C++."
type: docs
weight: 78000
url: /ar/cpp/aspose.words/ihyphenationcallback/
---
## IHyphenationCallback interface


يُنفّذ من قبل الفئات التي يمكنها تسجيل قواميس التجزئة.

```cpp
class IHyphenationCallback : public virtual System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [RequestDictionary](./requestdictionary/)(System::String) | يُخطر التطبيق بأن قاموس التجزئة للغة المحددة لم يُعثر عليه وقد يحتاج إلى التسجيل. يجب على التنفيذ العثور على القاموس وتسجيله باستخدام طرق [RegisterDictionary()](../). إذا كان القاموس غير متوفر للغة المحددة، يمكن للتنفيذ إلغاء الاستدعاءات اللاحقة لنفس اللغة باستخدام [RegisterDictionary()](../) مع القيمة **null**. |
| static [Type](./type/)() |  |
## انظر أيضًا

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
