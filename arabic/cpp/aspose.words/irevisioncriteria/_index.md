---
title: "Aspose::Words::IRevisionCriteria واجهة"
linktitle: "IRevisionCriteria"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::IRevisionCriteria واجهة. نفّذ هذه الواجهة إذا كنت تريد التحكم في متى يجب قبول/رفض Revision معينة أو لا بواسطة طريقتي Accept()/Reject() في C++."
type: docs
weight: 79500
url: /ar/cpp/aspose.words/irevisioncriteria/
---
## IRevisionCriteria interface


نفّذ هذه الواجهة إذا كنت تريد التحكم في متى يجب قبول/رفض [Revision](../revision/) معينة أو لا بواسطة طريقتي [Accept()](../) و[Reject()](../).

```cpp
class IRevisionCriteria : public virtual System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [IsMatch](./ismatch/)(System::SharedPtr\<Aspose::Words::Revision\>) | يتحقق مما إذا كان *revision* المحدد يطابق المعايير أم لا. |
| static [Type](./type/)() |  |
## انظر أيضًا

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
