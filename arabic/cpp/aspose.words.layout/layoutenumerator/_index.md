---
title: "فئة Aspose::Words::Layout::LayoutEnumerator."
linktitle: "LayoutEnumerator"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::Layout::LayoutEnumerator. تُعدّ كائنات تخطيط الصفحة في المستند. يمكنك استخدام هذه الفئة للتنقل عبر نموذج تخطيط الصفحة. الخصائص المتاحة هي النوع، الهندسة، النص ومؤشر الصفحة حيث يتم عرض الكائن، بالإضافة إلى الهيكل العام والعلاقات. استخدم الجمع بين GetEntity() وCurrent للانتقال إلى الكائن الذي يتCorrespond إلى عقدة المستند. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.layout/layoutenumerator/
---
## LayoutEnumerator class


تُعدّ كائنات تخطيط الصفحة في مستند. يمكنك استخدام هذه الفئة للتنقل عبر نموذج تخطيط الصفحة. الخصائص المتاحة هي النوع، الهندسة، النص ومؤشر الصفحة حيث يتم عرض الكائن، بالإضافة إلى الهيكل العام والعلاقات. استخدم الجمع بين [GetEntity()](../) و[Current](./get_current/) للانتقال إلى الكائن الذي يتCorrespond إلى عقدة المستند. لمعرفة المزيد، زر مقالة الوثائق [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/).

```cpp
class LayoutEnumerator : public System::Object,
                         public System::Details::EnumeratorBasedIterator<System::SharedPtr<System::Object>>,
                         private System::Details::IteratorPointerUpdater<System::SharedPtr<System::Object>, false>
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [CloneIterator](./cloneiterator/)() const override |  |
| [get_Current](./get_current/)() const | يحصل على أو يعيّن الموضع الحالي في نموذج تخطيط الصفحة. تُعيد هذه الخاصية كائنًا غير شفاف يتCorrespond إلى كائن التخطيط الحالي. |
| [get_Document](./get_document/)() const | يحصل على المستند الذي تُعدّ هذه الحالة. |
| [get_Kind](./get_kind/)() | يحصل على نوع الكيان الحالي. يمكن أن يكون سلسلة فارغة ولكن لا يكون أبداً **null**. |
| [get_PageIndex](./get_pageindex/)() | يحصل على المؤشر بدءًا من 1 للصفحة التي تحتوي على الكيان الحالي. |
| [get_Rectangle](./get_rectangle/)() | يرجع المستطيل الحدودي للكيان الحالي بالنسبة إلى الزاوية العليا اليسرى للصفحة (بالنقاط). |
| [get_Text](./get_text/)() | يحصل على نص الكيان الحالي من النوع Span. يرمي استثناءً للأنواع الأخرى من الكيانات. |
| [get_Type](./get_type/)() | يحصل على نوع الكيان الحالي. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(const System::String\&) | يحصل على خاصية مسماة للكيان. |
| [IncrementIterator](./incrementiterator/)() override |  |
| [InitializeIterator](./initializeiterator/)() override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [LayoutEnumerator](./layoutenumerator/)(const System::SharedPtr\<Aspose::Words::Document\>\&) | يُنشئ نسخة جديدة من هذه الفئة. |
| [MoveFirstChild](./movefirstchild/)() | ينتقل إلى أول كيان فرعي. |
| [MoveLastChild](./movelastchild/)() | ينتقل إلى آخر كيان فرعي. |
| [MoveNext](./movenext/)() | ينتقل إلى الكيان الشقيق التالي بترتيب بصري. عند تكرار أسطر فقرة مقسمة عبر صفحات، لن ينتقل هذا الأسلوب إلى الصفحة التالية بل ينتقل إلى الكيان التالي على نفس الصفحة. |
| [MoveNextLogical](./movenextlogical/)() | ينتقل إلى الكيان الشقيق التالي بترتيب منطقي. عند تكرار أسطر فقرة مقسمة عبر صفحات، سيقوم هذا الأسلوب بالانتقال إلى السطر التالي حتى وإن كان موجودًا في صفحة أخرى. |
| [MoveParent](./moveparent/)() | ينتقل إلى الكيان الأب. |
| [MoveParent](./moveparent/)(Aspose::Words::Layout::LayoutEntityType) | ينتقل إلى الكيان الأب من النوع المحدد. |
| [MovePrevious](./moveprevious/)() | ينتقل إلى الكيان الشقيق السابق. |
| [MovePreviousLogical](./movepreviouslogical/)() | ينتقل إلى الكيان الشقيق السابق بترتيب منطقي. عند تكرار أسطر فقرة مقسمة عبر صفحات، سيقوم هذا الأسلوب بالانتقال إلى السطر السابق حتى وإن كان موجودًا في صفحة أخرى. |
| [Reset](./reset/)() | ينقل المُعدِّد إلى الصفحة الأولى من المستند. |
| [set_Current](./set_current/)(const System::SharedPtr\<System::Object\>\&) | مُعيّن لـ [Aspose::Words::Layout::LayoutEnumerator::get_Current](./get_current/). |
| static [Type](./type/)() |  |
## انظر أيضًا

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
