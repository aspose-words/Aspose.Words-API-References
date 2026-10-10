---
title: "Aspose::Words::DocumentBuilder::MoveToSection method"
linktitle: "MoveToSection"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::DocumentBuilder::MoveToSection method. ينقل المؤشر إلى بداية الجسم في قسم محدد في C++."
type: docs
weight: 60000
url: /ar/cpp/aspose.words/documentbuilder/movetosection/
---
## DocumentBuilder::MoveToSection method


ينقل المؤشر إلى بداية النص في قسم محدد.

```cpp
void Aspose::Words::DocumentBuilder::MoveToSection(int32_t sectionIndex)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| sectionIndex | int32_t | فهرس القسم الذي سيتم الانتقال إليه. |
## ملاحظات


عندما يكون *sectionIndex* أكبر من أو يساوي 0، فإنه يحدد فهرساً من بداية المستند حيث 0 هو القسم الأول. عندما يكون *sectionIndex* أقل من 0، فإنه يحدد فهرساً من نهاية المستند حيث -1 هو القسم الأخير.

يتم نقل المؤشر إلى الفقرة الأولى في [Body](../../body/) للقسم المحدد.

## انظر أيضًا

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
