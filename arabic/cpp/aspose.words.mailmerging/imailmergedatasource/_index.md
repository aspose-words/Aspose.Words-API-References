---
title: "واجهة Aspose::Words::MailMerging::IMailMergeDataSource"
linktitle: "IMailMergeDataSource"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "واجهة Aspose::Words::MailMerging::IMailMergeDataSource. نفّذ هذه الواجهة للسماح بدمج البريد من مصدر بيانات مخصص، مثل قائمة من الكائنات. كما يتم دعم بيانات رئيس-تفصيل في C++."
type: docs
weight: 9000
url: /ar/cpp/aspose.words.mailmerging/imailmergedatasource/
---
## IMailMergeDataSource interface


نفّذ هذه الواجهة للسماح بدمج البريد من مصدر بيانات مخصص، مثل قائمة من الكائنات. كما يتم دعم بيانات رئيسية-تفصيلية.

```cpp
class IMailMergeDataSource : public virtual System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| virtual [get_TableName](./get_tablename/)() | ترجع اسم مصدر البيانات. |
| virtual [GetChildDataSource](./getchilddatasource/)(System::String) | محرك دمج البريد Aspose.Words يستدعي هذه الطريقة عندما يصادف بداية منطقة دمج بريد متداخلة. |
| [GetType](./gettype/)() const override |  |
| virtual [GetValue](./getvalue/)(System::String, System::SharedPtr\<System::Object\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [MoveNext](./movenext/)() | يتقدم إلى السجل التالي في مصدر البيانات. |
| static [Type](./type/)() |  |
## ملاحظات


عند إنشاء مصدر بيانات، يجب تهيئته للإشارة إلى BOF (قبل السجل الأول). محرك دمج البريد Aspose.Words سيستدعي [MoveNext](./movenext/) للتقدم إلى السجل التالي ثم يستدعي [GetValue()](./getvalue/) لكل حقل دمج يصادفه في المستند أو منطقة دمج البريد الحالية.

## انظر أيضًا

* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
