---
title: "Aspose::Words::Fields::IFieldUpdatingCallback interface"
linktitle: "IFieldUpdatingCallback"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fields::IFieldUpdatingCallback interface. نفّذ هذه الواجهة إذا كنت تريد أن تُستدعى طرقك المخصصة أثناء تحديث الحقل في C++."
type: docs
weight: 123000
url: /ar/cpp/aspose.words.fields/ifieldupdatingcallback/
---
## IFieldUpdatingCallback interface


نفّذ هذه الواجهة إذا أردت أن تُستدعى طرقك المخصصة الخاصة أثناء تحديث الحقل.

```cpp
class IFieldUpdatingCallback : public virtual System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| virtual [FieldUpdated](./fieldupdated/)(System::SharedPtr\<Aspose::Words::Fields::Field\>) | طريقة معرفة من قبل المستخدم تُستدعى مباشرةً بعد تحديث الحقل. |
| virtual [FieldUpdating](./fieldupdating/)(System::SharedPtr\<Aspose::Words::Fields::Field\>) | طريقة معرفة من قبل المستخدم تُستدعى مباشرةً قبل تحديث الحقل. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## انظر أيضًا

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
