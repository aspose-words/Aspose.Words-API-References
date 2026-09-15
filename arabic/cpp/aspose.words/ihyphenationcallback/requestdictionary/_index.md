---
title: "طريقة Aspose::Words::IHyphenationCallback::RequestDictionary. تُخطر التطبيق بأن قاموس التجزئة للغة المحددة لم يُعثر عليه وقد يحتاج إلى التسجيل. يجب على التنفيذ العثور على قاموس وتسجيله باستخدام طرق RegisterDictionary(). إذا كان القاموس غير متوفر للغة المحددة يمكن للتنفيذ إلغاء المزيد من الاستدعاءات لنفس اللغة باستخدام RegisterDictionary() بقيمة null في C++."
linktitle: "طريقة Aspose::Words::IHyphenationCallback::GetType"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "كيفية استخدام طريقة GetType لفئة Aspose::Words::IHyphenationCallback في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words/ihyphenationcallback/requestdictionary/
---
## IHyphenationCallback::RequestDictionary method


يُخطر التطبيق بأن قاموس التجزئة للغة المحددة لم يُعثر عليه وقد يحتاج إلى التسجيل. يجب على التنفيذ العثور على القاموس وتسجيله باستخدام طرق [RegisterDictionary()](../). إذا كان القاموس غير متوفر للغة المحددة، يمكن للتنفيذ إلغاء الاستدعاءات اللاحقة لنفس اللغة باستخدام [RegisterDictionary()](../) مع القيمة **null**.

```cpp
virtual void Aspose::Words::IHyphenationCallback::RequestDictionary(System::String language)=0
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| اللغة | System::String | اسم لغة، على سبيل المثال "en-US". راجع وثائق .NET للحصول على "اسم الثقافة" وRFC 4646 للتفاصيل. |

## انظر أيضًا

* Interface [IHyphenationCallback](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
