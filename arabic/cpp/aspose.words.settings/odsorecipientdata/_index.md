---
title: "فئة Aspose::Words::Settings::OdsoRecipientData"
linktitle: "OdsoRecipientData"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::Settings::OdsoRecipientData. تمثّل معلومات حول سجل واحد داخل مصدر بيانات خارجي يجب استبعاده من دمج البريد. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 7000
url: /ar/cpp/aspose.words.settings/odsorecipientdata/
---
## OdsoRecipientData class


يمثل معلومات حول سجل واحد داخل مصدر بيانات خارجي يجب استثناؤه من الدمج البريدي. لمعرفة المزيد، زر مقالة الوثائق [Mail Merge and Reporting](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/).

```cpp
class OdsoRecipientData : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [Clone](./clone/)() | يرجع نسخة عميقة من هذا الكائن. |
| [get_Active](./get_active/)() const | يحدد ما إذا كان السجل من مصدر البيانات سيُستورد إلى مستند عند تنفيذ دمج البريد. القيمة الافتراضية هي **true**. |
| [get_Column](./get_column/)() const | يحدد العمود داخل مصدر البيانات الذي يحتوي على بيانات فريدة للسجل الحالي. القيمة الافتراضية هي 0. |
| [get_Hash](./get_hash/)() const | يمثّل رمز التجزئة لهذا السجل. أحيانًا يستخدم Microsoft Word [Hash](./get_hash/) لسجل كامل بدلاً من قيمة [UniqueTag](./get_uniquetag/). القيمة الافتراضية هي 0. |
| [get_UniqueTag](./get_uniquetag/)() const | يحدد محتويات سجل معين في العمود الذي يحتوي على بيانات فريدة. القيمة الافتراضية هي **null**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [OdsoRecipientData](./odsorecipientdata/)() |  |
| [set_Active](./set_active/)(bool) | يحدد ما إذا كان السجل من مصدر البيانات سيُستورد إلى مستند عند تنفيذ دمج البريد. القيمة الافتراضية هي **true**. |
| [set_Column](./set_column/)(int32_t) | يحدد العمود داخل مصدر البيانات الذي يحتوي على بيانات فريدة للسجل الحالي. القيمة الافتراضية هي 0. |
| [set_Hash](./set_hash/)(int32_t) | يمثّل رمز التجزئة لهذا السجل. أحيانًا يستخدم Microsoft Word [Hash](./get_hash/) لسجل كامل بدلاً من قيمة [UniqueTag](./get_uniquetag/). القيمة الافتراضية هي 0. |
| [set_UniqueTag](./set_uniquetag/)(const System::ArrayPtr\<uint8_t\>\&) | يحدد محتويات سجل معين في العمود الذي يحتوي على بيانات فريدة. القيمة الافتراضية هي **null**. |
| static [Type](./type/)() |  |
## ملاحظات


إذا كان يجب دمج سجل في مستند مدمج، فلا يلزم أي معلومات عن ذلك السجل. ومع ذلك، إذا كان يجب عدم دمج سجل معين في مستند مدمج، فيجب تخزين قيمة المفتاح الفريد لذلك السجل في خاصية [UniqueTag](./get_uniquetag/) لهذا الكائن للإشارة إلى هذا الاستبعاد.
## انظر أيضًا

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
