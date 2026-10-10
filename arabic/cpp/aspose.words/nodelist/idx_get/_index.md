---
title: "Aspose::Words::NodeList::idx_get طريقة"
linktitle: "idx_get"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::NodeList::idx_get طريقة. يسترجع عقدة عند الفهرس المعطى في C++."
type: docs
weight: 6000
url: /ar/cpp/aspose.words/nodelist/idx_get/
---
## NodeList::idx_get method


يسترجع عقدة في الفهرس المحدد.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::NodeList::idx_get(int32_t index) const
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| index | int32_t | فهرس في قائمة العقد. |
## ملاحظات


الفهرس يبدأ من الصفر.

يسمح باستخدام الفهارس السلبية وتدل على الوصول من نهاية المجموعة. على سبيل المثال -1 يعني العنصر الأخير، -2 يعني العنصر قبل الأخير، وهكذا.

إذا كان الفهرس أكبر من أو يساوي عدد العناصر في القائمة، فإن هذا يُرجع إشارة فارغة.

إذا كان الفهرس سالبًا وكانت قيمته المطلقة أكبر من عدد العناصر في القائمة، فإن هذا يُرجع إشارة فارغة.

## انظر أيضًا

* Class [Node](../../node/)
* Class [NodeList](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
