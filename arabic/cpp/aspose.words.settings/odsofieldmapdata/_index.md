---
title: "Aspose::Words::Settings::OdsoFieldMapData class"
linktitle: "OdsoFieldMapData"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Settings::OdsoFieldMapData class. تحدد كيفية ربط عمود في مصدر البيانات الخارجي بالحقول المدمجة المعرفة مسبقًا داخل المستند. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words.settings/odsofieldmapdata/
---
## OdsoFieldMapData class


يحدد كيفية ربط عمود في مصدر البيانات الخارجي بالحقول المدمجة المحددة مسبقًا داخل المستند. لمعرفة المزيد، زر مقالة الوثائق [Mail Merge and Reporting](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/).

```cpp
class OdsoFieldMapData : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [Clone](./clone/)() | يرجع نسخة عميقة من هذا الكائن. |
| [get_Column](./get_column/)() const | تحدد الفهرس الصفري للعمود داخل مصدر بيانات خارجي والذي سيتم ربطه بالاسم المحلي لحقل MERGEFIELD محدد. القيمة الافتراضية هي 0. |
| [get_MappedName](./get_mappedname/)() const | تحدد اسم الحقل المدمج المعرفة مسبقًا والذي سيتم ربطه برقم العمود المحدد بواسطة الخاصية [Column](./get_column/) داخل هذا التخطيط. القيمة الافتراضية هي سلسلة فارغة. |
| [get_Name](./get_name/)() const | تحدد اسم العمود داخل مصدر بيانات خارجي للعمود الذي يُحدَّد فهرسه بواسطة الخاصية [Column](./get_column/). القيمة الافتراضية هي سلسلة فارغة. |
| [get_Type](./get_type/)() const | تحدد ما إذا كان حقل دمج البريد المحدد قد تم ربطه بعمود في مصدر البيانات الخارجي المعطى أم لا. القيمة الافتراضية هي [Default](../odsofieldmappingtype/). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [OdsoFieldMapData](./odsofieldmapdata/)() |  |
| [set_Column](./set_column/)(int32_t) | تحدد الفهرس الصفري للعمود داخل مصدر بيانات خارجي والذي سيتم ربطه بالاسم المحلي لحقل MERGEFIELD محدد. القيمة الافتراضية هي 0. |
| [set_MappedName](./set_mappedname/)(const System::String\&) | تحدد اسم الحقل المدمج المعرفة مسبقًا والذي سيتم ربطه برقم العمود المحدد بواسطة الخاصية [Column](./get_column/) داخل هذا التخطيط. القيمة الافتراضية هي سلسلة فارغة. |
| [set_Name](./set_name/)(const System::String\&) | تحدد اسم العمود داخل مصدر بيانات خارجي للعمود الذي يُحدَّد فهرسه بواسطة الخاصية [Column](./get_column/). القيمة الافتراضية هي سلسلة فارغة. |
| [set_Type](./set_type/)(Aspose::Words::Settings::OdsoFieldMappingType) | تحدد ما إذا كان حقل دمج البريد المحدد قد تم ربطه بعمود في مصدر البيانات الخارجي المعطى أم لا. القيمة الافتراضية هي [Default](../odsofieldmappingtype/). |
| static [Type](./type/)() |  |
## ملاحظات


يوفر Microsoft Word بعض أسماء الحقول المدمجة المعرفة مسبقًا التي يمكن إدراجها في مستند كـ MERGEFIELD أو استخدامها في حقول ADDRESSBLOCK أو GREETINGLINE. المعلومات المحددة في [OdsoFieldMapData](./) تسمح بربط عمود واحد في مصدر البيانات الخارجي بحقل مدمج معرف مسبقًا.

## انظر أيضًا

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
