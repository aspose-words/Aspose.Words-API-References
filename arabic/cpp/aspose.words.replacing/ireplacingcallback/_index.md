---
title: "Aspose::Words::Replacing::IReplacingCallback interface"
linktitle: "IReplacingCallback"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Replacing::IReplacingCallback interface. نفّذ هذه الواجهة إذا كنت ترغب في الحصول على طريقة مخصصة خاصة بك تُستدعى أثناء عملية البحث والاستبدال في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.replacing/ireplacingcallback/
---
## IReplacingCallback interface


نفّذ هذه الواجهة إذا كنت ترغب في وجود طريقة مخصصة خاصة بك تُستدعى أثناء عملية البحث والاستبدال.

```cpp
class IReplacingCallback : public virtual System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Replacing](./replacing/)(System::SharedPtr\<Aspose::Words::Replacing::ReplacingArgs\>) | طريقة معرفة من قبل المستخدم تُستدعى أثناء عملية الاستبدال لكل مطابقة تم العثور عليها مباشرةً قبل إجراء الاستبدال. |
| static [Type](./type/)() |  |
## انظر أيضًا

* Namespace [Aspose::Words::Replacing](../)
* Library [Aspose.Words for C++](../../)
