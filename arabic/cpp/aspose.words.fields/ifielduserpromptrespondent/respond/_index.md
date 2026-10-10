---
title: "طريقة Aspose::Words::Fields::IFieldUserPromptRespondent::Respond"
linktitle: "Respond"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Fields::IFieldUserPromptRespondent::Respond. عند تنفيذها، تُعيد استجابة من المستخدم عند الطلب. يجب أن تُعيد تنفيذتك القيمة null للإشارة إلى أن المستخدم لم يرد على الطلب (أي أن المستخدم ضغط زر إلغاء في نافذة الطلب) في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words.fields/ifielduserpromptrespondent/respond/
---
## IFieldUserPromptRespondent::Respond method


عند التنفيذ، تُعيد استجابة من المستخدم عند المطالبة. يجب على تنفيذك إرجاع **null** للدلالة على أن المستخدم لم يرد على المطالبة (أي أن المستخدم ضغط زر الإلغاء في نافذة المطالبة).

```cpp
virtual System::String Aspose::Words::Fields::IFieldUserPromptRespondent::Respond(System::String promptText, System::String defaultResponse)=0
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| promptText | System::String | نص الطلب (أي عنوان نافذة الطلب). |
| defaultResponse | System::String | استجابة المستخدم الافتراضية (أي القيمة الأولية الموجودة في نافذة الطلب). |

### ReturnValue

استجابة المستخدم (أي القيمة المؤكدة الموجودة في نافذة الطلب).

## انظر أيضًا

* Interface [IFieldUserPromptRespondent](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
