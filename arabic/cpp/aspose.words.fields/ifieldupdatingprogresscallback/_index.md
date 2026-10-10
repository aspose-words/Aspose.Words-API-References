---
title: "Aspose::Words::Fields::IFieldUpdatingProgressCallback واجهة"
linktitle: "IFieldUpdatingProgressCallback"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fields::IFieldUpdatingProgressCallback واجهة. نفّذ هذه الواجهة إذا أردت تتبع تقدم تحديث الحقول في C++."
type: docs
weight: 124000
url: /ar/cpp/aspose.words.fields/ifieldupdatingprogresscallback/
---
## IFieldUpdatingProgressCallback interface


نفّذ هذه الواجهة إذا أردت تتبع تقدم تحديث الحقل.

```cpp
class IFieldUpdatingProgressCallback : public virtual System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Notify](./notify/)(System::SharedPtr\<Aspose::Words::Fields::FieldUpdatingProgressArgs\>) | طريقة معرفة من قبل المستخدم تُستدعى عندما يتغير تقدم التحديث. |
| static [Type](./type/)() |  |
## انظر أيضًا

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
