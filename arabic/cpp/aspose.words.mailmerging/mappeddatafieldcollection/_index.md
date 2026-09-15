---
title: "Aspose::Words::MailMerging::MappedDataFieldCollection فئة"
linktitle: "MappedDataFieldCollection"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::MailMerging::MappedDataFieldCollection فئة. يسمح بربط الأسماء بين حقول مصدر البيانات الخاص بك وأسماء حقول دمج البريد في المستند تلقائيًا. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 6000
url: /ar/cpp/aspose.words.mailmerging/mappeddatafieldcollection/
---
## MappedDataFieldCollection class


يسمح بربط تلقائي بين أسماء الحقول في مصدر البيانات الخاص بك وأسماء حقول دمج البريد في المستند. لمعرفة المزيد، زر مقالة الوثائق [Mail Merge and Reporting](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/).

```cpp
class MappedDataFieldCollection : public System::Collections::Generic::IEnumerable<System::Collections::Generic::KeyValuePair<System::String, System::String>>
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [Add](./add/)(const System::String\&, const System::String\&) | يضيف تعيين حقل جديد. |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | يزيل جميع العناصر من المجموعة. |
| [ContainsKey](./containskey/)(const System::String\&) | يحدد ما إذا كان هناك تعيين من الحقل المحدد في المستند موجودًا في المجموعة. |
| [ContainsValue](./containsvalue/)(const System::String\&) | يحدد ما إذا كان هناك تعيين من الحقل المحدد في مصدر البيانات موجودًا في المجموعة. |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | يحصل على عدد العناصر الموجودة في المجموعة. |
| [GetEnumerator](./getenumerator/)() override | يرجع كائن عداد القاموس الذي يمكن استخدامه للتنقل عبر جميع العناصر في المجموعة. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(const System::String\&) | يحصل أو يضبط اسم الحقل في مصدر البيانات المرتبط بحقل دمج البريد المحدد. |
| [idx_set](./idx_set/)(const System::String\&, const System::String\&) | يحصل أو يضبط اسم الحقل في مصدر البيانات المرتبط بحقل دمج البريد المحدد. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::String\&) | يزيل تعيين حقل. |
| static [Type](./type/)() |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
## Typedefs

| تعريف نوع | الوصف |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |
## ملاحظات


يتم تنفيذ ذلك كمجموعة من مفاتيح السلسلة إلى قيم السلسلة. المفاتيح هي أسماء حقول دمج البريد في المستند والقيم هي أسماء الحقول في مصدر البيانات الخاص بك.

## انظر أيضًا

* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
