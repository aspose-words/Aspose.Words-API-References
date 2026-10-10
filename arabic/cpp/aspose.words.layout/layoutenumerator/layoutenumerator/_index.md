---
title: "منشئ Aspose::Words::Layout::LayoutEnumerator::LayoutEnumerator"
linktitle: "LayoutEnumerator"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "منشئ Aspose::Words::Layout::LayoutEnumerator::LayoutEnumerator. يهيئ نسخة جديدة من هذه الفئة في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.layout/layoutenumerator/layoutenumerator/
---
## LayoutEnumerator::LayoutEnumerator constructor


يُنشئ نسخة جديدة من هذه الفئة.

```cpp
Aspose::Words::Layout::LayoutEnumerator::LayoutEnumerator(const System::SharedPtr<Aspose::Words::Document> &document)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| مستند | const System::SharedPtr\<Aspose::Words::Document\>\& | مستند يتم تعداد نموذج تخطيط الصفحات الخاص به. |
## ملاحظات


إذا لم يتم بناء نموذج تخطيط الصفحات للمستند، فإن المُعدِّد يستدعي [UpdatePageLayout](../../../aspose.words/document/updatepagelayout/) لبنائه.

كلما تم تحديث المستند وإنشاء نموذج تخطيط صفحات جديد، يجب استخدام مُعدِّد جديد للوصول إليه.

## انظر أيضًا

* Class [Document](../../../aspose.words/document/)
* Class [LayoutEnumerator](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
