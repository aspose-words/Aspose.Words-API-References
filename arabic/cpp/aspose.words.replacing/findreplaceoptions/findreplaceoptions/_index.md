---
title: "منشئ Aspose::Words::Replacing::FindReplaceOptions::FindReplaceOptions"
linktitle: "FindReplaceOptions"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "منشئ Aspose::Words::Replacing::FindReplaceOptions::FindReplaceOptions. يهيئ نسخة جديدة من فئة FindReplaceOptions بالإعدادات الافتراضية في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.replacing/findreplaceoptions/findreplaceoptions/
---
## FindReplaceOptions::FindReplaceOptions() constructor


يهيئ نسخة جديدة من الفئة [FindReplaceOptions](../) بالإعدادات الافتراضية.

```cpp
Aspose::Words::Replacing::FindReplaceOptions::FindReplaceOptions()
```


## أمثلة



يظهر كيفية التعرف على الاستبدالات واستخدامها داخل أنماط الاستبدال.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Jason gave money to Paul.");

auto regex = System::MakeObject<System::Text::RegularExpressions::Regex>(u"([A-z]+) gave money to ([A-z]+)");

auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
options->set_UseSubstitutions(true);

// استخدام وضع التوافق القديم لا يدعم العديد من الميزات المتقدمة، لذا نحتاج إلى ضبطه على 'false'.
options->set_LegacyMode(false);

doc->get_Range()->Replace(regex, u"$2 took money from $1", options);

ASSERT_EQ(doc->GetText(), u"Paul took money from Jason.\f");
```

## انظر أيضًا

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
## FindReplaceOptions::FindReplaceOptions(Aspose::Words::Replacing::FindReplaceDirection) constructor


يهيئ نسخة جديدة من الفئة [FindReplaceOptions](../) بالاتجاه المحدد.

```cpp
Aspose::Words::Replacing::FindReplaceOptions::FindReplaceOptions(Aspose::Words::Replacing::FindReplaceDirection direction)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| الاتجاه | Aspose::Words::Replacing::FindReplaceDirection | اتجاه عملية البحث والاستبدال. |

## انظر أيضًا

* Enum [FindReplaceDirection](../../findreplacedirection/)
* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
## FindReplaceOptions::FindReplaceOptions(Aspose::Words::Replacing::FindReplaceDirection, const System::SharedPtr\<Aspose::Words::Replacing::IReplacingCallback\>\&) constructor


يهيئ نسخة جديدة من الفئة [FindReplaceOptions](../) بالاتجاه المحدد ودالة الاستدعاء للاستبدال.

```cpp
Aspose::Words::Replacing::FindReplaceOptions::FindReplaceOptions(Aspose::Words::Replacing::FindReplaceDirection direction, const System::SharedPtr<Aspose::Words::Replacing::IReplacingCallback> &replacingCallback)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| الاتجاه | Aspose::Words::Replacing::FindReplaceDirection | اتجاه عملية البحث والاستبدال. |
| replacingCallback | const System::SharedPtr\<Aspose::Words::Replacing::IReplacingCallback\>\& | دالة الاستدعاء المستخدمة لاستبدال النص الموجود. |

## انظر أيضًا

* Enum [FindReplaceDirection](../../findreplacedirection/)
* Interface [IReplacingCallback](../../ireplacingcallback/)
* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
## FindReplaceOptions::FindReplaceOptions(const System::SharedPtr\<Aspose::Words::Replacing::IReplacingCallback\>\&) constructor


يهيئ نسخة جديدة من الفئة [FindReplaceOptions](../) بدالة الاستدعاء المحددة للاستبدال.

```cpp
Aspose::Words::Replacing::FindReplaceOptions::FindReplaceOptions(const System::SharedPtr<Aspose::Words::Replacing::IReplacingCallback> &replacingCallback)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| replacingCallback | const System::SharedPtr\<Aspose::Words::Replacing::IReplacingCallback\>\& | دالة الاستدعاء المستخدمة لاستبدال النص الموجود. |

## انظر أيضًا

* Interface [IReplacingCallback](../../ireplacingcallback/)
* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
