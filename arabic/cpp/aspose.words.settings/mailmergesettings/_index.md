---
title: "Aspose::Words::Settings::MailMergeSettings فئة"
linktitle: "MailMergeSettings"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Settings::MailMergeSettings فئة. يحدد جميع معلومات دمج البريد للمستند. لمزيد من المعلومات، قم بزيارة مقالة الوثائق في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.settings/mailmergesettings/
---
## MailMergeSettings class


يحدد جميع معلومات الدمج البريدي للمستند. لمعرفة المزيد، زر مقالة الوثائق [Mail Merge and Reporting](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/).

```cpp
class MailMergeSettings : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [Clear](./clear/)() | يمسح إعدادات دمج البريد بطريقة تجعل المستند عند حفظه لا يتم حفظ أي إعدادات دمج بريد ويصبح مستندًا عاديًا. |
| [Clone](./clone/)() | يرجع نسخة عميقة من هذا الكائن. |
| [get_ActiveRecord](./get_activerecord/)() const | يحدد الفهرس القائم على الواحد للسجل من مصدر البيانات الذي سيُعرض في Microsoft Word. القيمة الافتراضية هي 1. |
| [get_AddressFieldName](./get_addressfieldname/)() const | يحدد العمود داخل مصدر البيانات الذي يحتوي على عناوين البريد الإلكتروني. القيمة الافتراضية هي سلسلة فارغة. |
| [get_CheckErrors](./get_checkerrors/)() const | يحدد نوع تقارير الأخطاء التي سيجريها Microsoft Word عند تنفيذ دمج البريد. القيمة الافتراضية هي [Default](../mailmergecheckerrors/). |
| [get_ConnectString](./get_connectstring/)() const | يحدد سلسلة الاتصال المستخدمة للاتصال بمصدر بيانات خارجي. القيمة الافتراضية هي سلسلة فارغة. |
| [get_DataSource](./get_datasource/)() const | يحدد المسار إلى مصدر بيانات دمج البريد. القيمة الافتراضية هي سلسلة فارغة. |
| [get_DataType](./get_datatype/)() const | يحدد نوع مصدر بيانات دمج البريد وطريقة الوصول إلى البيانات. القيمة الافتراضية هي [Default](../mailmergedatatype/). |
| [get_Destination](./get_destination/)() const | يحدد كيفية إخراج Microsoft Word لنتائج دمج البريد. القيمة الافتراضية هي [Default](../mailmergedestination/). |
| [get_DoNotSupressBlankLines](./get_donotsupressblanklines/)() const | يحدد كيفية تعامل التطبيق الذي ينفذ دمج البريد مع الأسطر الفارغة في المستندات المدمجة الناتجة عن دمج البريد. القيمة الافتراضية هي **false**. |
| [get_HeaderSource](./get_headersource/)() const | يحدد المسار إلى مصدر رأس دمج البريد. القيمة الافتراضية هي سلسلة فارغة. |
| [get_LinkToQuery](./get_linktoquery/)() const | غير متأكد من هذا. تشير مرجع أتمتة Microsoft Word إلى أن هذا يحدد أن الاستعلام يُنفّذ في كل مرة يُفتح فيها المستند في Microsoft Word. لكن مواصفة OOXML تشير إلى أن هذا يحدد أن الاستعلام يحتوي على إشارة إلى ملف استعلام خارجي يحتوي على الاستعلام الفعلي. القيمة الافتراضية هي **false**. |
| [get_MailAsAttachment](./get_mailasattachment/)() const | يحدد أن المستندات التي تُنتج أثناء عملية دمج البريد يجب أن تُرسل كملف مرفق بدلاً من أن تكون في جسم البريد الإلكتروني الفعلي. القيمة الافتراضية هي **false**. |
| [get_MailSubject](./get_mailsubject/)() const | يحدد النص الذي سيظهر في سطر الموضوع للبريد الإلكتروني أو الفاكسات التي تُنتج أثناء دمج البريد. القيمة الافتراضية هي سلسلة فارغة. |
| [get_MainDocumentType](./get_maindocumenttype/)() const | يحدد نوع المستند الرئيسي لدمج البريد. القيمة الافتراضية هي [Default](../mailmergemaindocumenttype/). |
| [get_Odso](./get_odso/)() const | يحصل على الكائن الذي يحدد إعدادات Office Data Source Object (ODSO). |
| [get_Query](./get_query/)() const | يحتوي على سلسلة Structured Query Language التي سيتم تشغيلها ضد مصدر البيانات الخارجي المحدد لإرجاع مجموعة السجلات التي ستُستورد إلى المستند عند تنفيذ عملية دمج البريد. القيمة الافتراضية هي سلسلة فارغة. |
| [get_ViewMergedData](./get_viewmergeddata/)() const | يحدد أن Microsoft Word سيعرض البيانات من مصدر البيانات الخارجي المحدد حيث تم إدراج حقول الدمج (مثل معاينة البيانات المدمجة). القيمة الافتراضية هي **false**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [MailMergeSettings](./mailmergesettings/)() |  |
| [set_ActiveRecord](./set_activerecord/)(int32_t) | يحدد الفهرس القائم على الواحد للسجل من مصدر البيانات الذي سيُعرض في Microsoft Word. القيمة الافتراضية هي 1. |
| [set_AddressFieldName](./set_addressfieldname/)(const System::String\&) | يحدد العمود داخل مصدر البيانات الذي يحتوي على عناوين البريد الإلكتروني. القيمة الافتراضية هي سلسلة فارغة. |
| [set_CheckErrors](./set_checkerrors/)(Aspose::Words::Settings::MailMergeCheckErrors) | يحدد نوع تقارير الأخطاء التي سيجريها Microsoft Word عند تنفيذ دمج البريد. القيمة الافتراضية هي [Default](../mailmergecheckerrors/). |
| [set_ConnectString](./set_connectstring/)(const System::String\&) | يحدد سلسلة الاتصال المستخدمة للاتصال بمصدر بيانات خارجي. القيمة الافتراضية هي سلسلة فارغة. |
| [set_DataSource](./set_datasource/)(const System::String\&) | يحدد المسار إلى مصدر بيانات دمج البريد. القيمة الافتراضية هي سلسلة فارغة. |
| [set_DataType](./set_datatype/)(Aspose::Words::Settings::MailMergeDataType) | يحدد نوع مصدر بيانات دمج البريد وطريقة الوصول إلى البيانات. القيمة الافتراضية هي [Default](../mailmergedatatype/). |
| [set_Destination](./set_destination/)(Aspose::Words::Settings::MailMergeDestination) | يحدد كيفية إخراج Microsoft Word لنتائج دمج البريد. القيمة الافتراضية هي [Default](../mailmergedestination/). |
| [set_DoNotSupressBlankLines](./set_donotsupressblanklines/)(bool) | يحدد كيفية تعامل التطبيق الذي ينفذ دمج البريد مع الأسطر الفارغة في المستندات المدمجة الناتجة عن دمج البريد. القيمة الافتراضية هي **false**. |
| [set_HeaderSource](./set_headersource/)(const System::String\&) | يحدد المسار إلى مصدر رأس دمج البريد. القيمة الافتراضية هي سلسلة فارغة. |
| [set_LinkToQuery](./set_linktoquery/)(bool) | دالة تعيين لـ [Aspose::Words::Settings::MailMergeSettings::get_LinkToQuery](./get_linktoquery/). |
| [set_MailAsAttachment](./set_mailasattachment/)(bool) | يحدد أن المستندات التي تُنتج أثناء عملية دمج البريد يجب أن تُرسل كملف مرفق بدلاً من أن تكون في جسم البريد الإلكتروني الفعلي. القيمة الافتراضية هي **false**. |
| [set_MailSubject](./set_mailsubject/)(const System::String\&) | يحدد النص الذي سيظهر في سطر الموضوع للبريد الإلكتروني أو الفاكسات التي تُنتج أثناء دمج البريد. القيمة الافتراضية هي سلسلة فارغة. |
| [set_MainDocumentType](./set_maindocumenttype/)(Aspose::Words::Settings::MailMergeMainDocumentType) | دالة تعيين لـ [Aspose::Words::Settings::MailMergeSettings::get_MainDocumentType](./get_maindocumenttype/). |
| [set_Odso](./set_odso/)(const System::SharedPtr\<Aspose::Words::Settings::Odso\>\&) | يضبط الكائن الذي يحدد إعدادات Office Data Source Object (ODSO). |
| [set_Query](./set_query/)(const System::String\&) | يحتوي على سلسلة Structured Query Language التي سيتم تشغيلها ضد مصدر البيانات الخارجي المحدد لإرجاع مجموعة السجلات التي ستُستورد إلى المستند عند تنفيذ عملية دمج البريد. القيمة الافتراضية هي سلسلة فارغة. |
| [set_ViewMergedData](./set_viewmergeddata/)(bool) | يحدد أن Microsoft Word سيعرض البيانات من مصدر البيانات الخارجي المحدد حيث تم إدراج حقول الدمج (مثل معاينة البيانات المدمجة). القيمة الافتراضية هي **false**. |
| static [Type](./type/)() |  |
## ملاحظات


يمكنك استخدام هذا الكائن لتحديد مصدر بيانات دمج البريد لمستند، وستظهر هذه المعلومات (إلى جانب حقول البيانات المتاحة) في Microsoft Word عندما يفتح المستخدم هذا المستند. أو يمكنك استخدام هذا الكائن لاستعلام إعدادات دمج البريد التي حددها المستخدم في Microsoft Word لهذا المستند.

عادةً لا تحتاج إلى إنشاء كائنات من هذه الفئة مباشرةً لأن إعدادات دمج البريد للمستند تكون دائمًا متاحة عبر خاصية [MailMergeSettings](../../aspose.words/document/get_mailmergesettings/).

لكشف ما إذا كان هذا المستند هو مستند دمج بريد رئيسي، تحقق من قيمة خاصية [MainDocumentType](./get_maindocumenttype/).

لإزالة إعدادات دمج البريد ومعلومات مصدر البيانات من مستند يمكنك استخدام طريقة [Clear](./clear/). لن تقوم Aspose.Words بكتابة إعدادات دمج البريد إلى مستند إذا تم تعيين خاصية [MainDocumentType](./get_maindocumenttype/) إلى [NotAMergeDocument](../mailmergemaindocumenttype/) أو تم تعيين خاصية [DataType](./get_datatype/) إلى [None](../mailmergedatatype/).

أفضل طريقة لتعلم كيفية استخدام خصائص هذا الكائن هي إنشاء مستند بمصدر بيانات مطلوب يدويًا في Microsoft Word ثم فتح ذلك المستند باستخدام Aspose.Words وفحص خصائص كائنات [MailMergeSettings](../../aspose.words/document/get_mailmergesettings/) و[Odso](./get_odso/). هذه طريقة جيدة إذا كنت ترغب في تعلم كيفية تكوين مصدر بيانات برمجيًا، على سبيل المثال.

تحافظ Aspose.Words على معلومات دمج البريد عند تحميل وحفظ وتحويل المستندات بين صيغ مختلفة، لكنها لا تستخدم هذه المعلومات عند إجراء دمج البريد الخاص بها باستخدام كائن [MailMerge](../../aspose.words.mailmerging/mailmerge/).

## انظر أيضًا

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
