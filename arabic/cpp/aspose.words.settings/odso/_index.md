---
title: "Aspose::Words::Settings::Odso class"
linktitle: "Odso"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Settings::Odso class. يحدد إعدادات كائن مصدر بيانات Office (ODSO) لمصدر بيانات دمج البريد. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words.settings/odso/
---
## Odso class


يحدد إعدادات كائن مصدر بيانات Office (ODSO) لمصدر بيانات الدمج البريدي. لمعرفة المزيد، زر مقالة الوثائق [Mail Merge and Reporting](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/).

```cpp
class Odso : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [Clone](./clone/)() | يرجع نسخة عميقة من هذا الكائن. |
| [get_ColumnDelimiter](./get_columndelimiter/)() const | يحدد الحرف الذي سيُفسَّر كفاصل أعمدة يُستخدم لفصل الأعمدة داخل مصادر البيانات الخارجية. القيمة الافتراضية هي 0 مما يعني عدم تعريف فاصل أعمدة. |
| [get_DataSource](./get_datasource/)() const | يحدد موقع مصدر البيانات الخارجي الذي سيُربط بالمستند لتنفيذ دمج البريد. القيمة الافتراضية هي سلسلة فارغة. |
| [get_DataSourceType](./get_datasourcetype/)() const | يحدد نوع مصدر البيانات الخارجي الذي سيُربط كجزء من معلومات اتصال ODSO لهذا دمج البريد. القيمة الافتراضية هي [Default](../odsodatasourcetype/). |
| [get_FieldMapDatas](./get_fieldmapdatas/)() const | يحصل على مجموعة من الكائنات التي تحدد كيفية ربط الأعمدة من مصدر البيانات الخارجي بأسماء حقول الدمج المعرفة مسبقًا في المستند. هذا الكائن لا يكون أبدًا **null**. |
| [get_FirstRowContainsColumnNames](./get_firstrowcontainscolumnnames/)() const | يحدد أن التطبيق المستضيف يجب أن يتعامل مع الصف الأول من البيانات في مصدر البيانات الخارجي المحدد كصف رأس يحتوي على أسماء كل عمود في مصدر البيانات. القيمة الافتراضية هي **false**. |
| [get_RecipientDatas](./get_recipientdatas/)() const | يحصل على مجموعة من الكائنات التي تحدد تضمين/استبعاد السجلات الفردية في دمج البريد. هذا الكائن لا يكون أبدًا **null**. |
| [get_TableName](./get_tablename/)() const | يحدد مجموعة البيانات المحددة التي يجب ربط المصدر بها داخل مصدر بيانات خارجي. القيمة الافتراضية هي سلسلة فارغة. |
| [get_UdlConnectString](./get_udlconnectstring/)() const | يحدد سلسلة اتصال Universal Data Link (UDL) المستخدمة للاتصال بمصدر بيانات خارجي. القيمة الافتراضية هي سلسلة فارغة. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Odso](./odso/)() |  |
| [set_ColumnDelimiter](./set_columndelimiter/)(char16_t) | المُعيّن لـ [Aspose::Words::Settings::Odso::get_ColumnDelimiter](./get_columndelimiter/). |
| [set_DataSource](./set_datasource/)(const System::String\&) | يحدد موقع مصدر البيانات الخارجي الذي سيُربط بالمستند لتنفيذ دمج البريد. القيمة الافتراضية هي سلسلة فارغة. |
| [set_DataSourceType](./set_datasourcetype/)(Aspose::Words::Settings::OdsoDataSourceType) | المُعيّن لـ [Aspose::Words::Settings::Odso::get_DataSourceType](./get_datasourcetype/). |
| [set_FieldMapDatas](./set_fieldmapdatas/)(const System::SharedPtr\<Aspose::Words::Settings::OdsoFieldMapDataCollection\>\&) | يضبط مجموعة من الكائنات التي تحدد كيفية ربط الأعمدة من مصدر البيانات الخارجي بأسماء حقول الدمج المعرفة مسبقًا في المستند. هذا الكائن لا يكون أبدًا **null**. |
| [set_FirstRowContainsColumnNames](./set_firstrowcontainscolumnnames/)(bool) | المُعيّن لـ [Aspose::Words::Settings::Odso::get_FirstRowContainsColumnNames](./get_firstrowcontainscolumnnames/). |
| [set_RecipientDatas](./set_recipientdatas/)(const System::SharedPtr\<Aspose::Words::Settings::OdsoRecipientDataCollection\>\&) | يضبط مجموعة من الكائنات التي تحدد تضمين/استبعاد السجلات الفردية في دمج البريد. هذا الكائن لا يكون أبدًا **null**. |
| [set_TableName](./set_tablename/)(const System::String\&) | يحدد مجموعة البيانات المحددة التي يجب ربط المصدر بها داخل مصدر بيانات خارجي. القيمة الافتراضية هي سلسلة فارغة. |
| [set_UdlConnectString](./set_udlconnectstring/)(const System::String\&) | يحدد سلسلة اتصال Universal Data Link (UDL) المستخدمة للاتصال بمصدر بيانات خارجي. القيمة الافتراضية هي سلسلة فارغة. |
| static [Type](./type/)() |  |
## ملاحظات


يبدو أن ODSO هو الطريقة "الجديدة" التي تفضّل إصدارات Microsoft Word الحديثة استخدامها عند تحديد أنواع معينة من مصادر البيانات لمستند دمج البريد. ربما ظهر ODSO لأول مرة في Microsoft Word 2000.

استخدام ODSO موثّق بشكل ضعيف وأفضل طريقة لتعلم كيفية استخدام خصائص هذا الكائن هي إنشاء مستند بمصدر بيانات مطلوب يدويًا في Microsoft Word ثم فتح ذلك المستند باستخدام Aspose.Words وفحص خصائص كائنات [MailMergeSettings](../../aspose.words/document/get_mailmergesettings/) و[Odso](../mailmergesettings/get_odso/). هذه طريقة جيدة إذا كنت ترغب في تعلم كيفية تكوين مصدر بيانات برمجيًا، على سبيل المثال.

عادةً لا تحتاج إلى إنشاء كائنات من هذه الفئة مباشرةً لأن إعدادات ODSO متاحة دائمًا عبر الخاصية [Odso](../mailmergesettings/get_odso/).

## انظر أيضًا

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
