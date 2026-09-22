---
title: "Aspose::Words::Fields::IFieldUserPromptRespondent interface"
linktitle: "IFieldUserPromptRespondent"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fields::IFieldUserPromptRespondent interface. يمثل المستجيب لمطالبات المستخدم أثناء تحديث الحقل في C++."
type: docs
weight: 125000
url: /ar/cpp/aspose.words.fields/ifielduserpromptrespondent/
---
## IFieldUserPromptRespondent interface


يمثل المستجيب لمطالبات المستخدم أثناء تحديث الحقل.

```cpp
class IFieldUserPromptRespondent : public virtual System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Respond](./respond/)(System::String, System::String) | عند التنفيذ، تُعيد استجابة من المستخدم عند المطالبة. يجب على تنفيذك إرجاع **null** للدلالة على أن المستخدم لم يرد على المطالبة (أي أن المستخدم ضغط زر الإلغاء في نافذة المطالبة). |
| static [Type](./type/)() |  |
## انظر أيضًا

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
