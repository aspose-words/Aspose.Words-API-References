---
title: "Aspose::Words::NodeList::ToArray طريقة"
linktitle: "ToArray"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::NodeList::ToArray طريقة. ينسخ جميع العقد من المجموعة إلى مصفوفة جديدة من العقد في C++."
type: docs
weight: 8000
url: /ar/cpp/aspose.words/nodelist/toarray/
---
## NodeList::ToArray method


ينسخ جميع العقد من المجموعة إلى مصفوفة جديدة من العقد.

```cpp
System::ArrayPtr<System::SharedPtr<Aspose::Words::Node>> Aspose::Words::NodeList::ToArray() const
```


### ReturnValue

مصفوفة من العقد.
## ملاحظات


يجب ألا تقوم بإضافة/إزالة العقد أثناء التكرار على مجموعة من العقد لأن ذلك يبطل المكرر ويتطلب تحديثات للمجموعات الحية.

لكي تتمكن من إضافة/إزالة العقد أثناء التكرار، استخدم هذه الطريقة لنسخ العقد إلى مصفوفة ثابتة الحجم ثم التكرار فوق المصفوفة.

## انظر أيضًا

* Class [Node](../../node/)
* Class [NodeList](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
