---
title: "Aspose::Words::Layout::IPageLayoutCallback واجهة"
linktitle: "IPageLayoutCallback"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Layout::IPageLayoutCallback واجهة. نفّذ هذه الواجهة إذا كنت تريد أن يكون لديك طريقتك المخصصة التي تُستدعى أثناء بناء وعرض نموذج تخطيط الصفحة في C++."
type: docs
weight: 6000
url: /ar/cpp/aspose.words.layout/ipagelayoutcallback/
---
## IPageLayoutCallback interface


قم بتنفيذ هذه الواجهة إذا كنت تريد أن يكون لديك طريقة مخصصة تُستدعى أثناء بناء وعرض نموذج تخطيط الصفحة.

```cpp
class IPageLayoutCallback : public virtual System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Notify](./notify/)(System::SharedPtr\<Aspose::Words::Layout::PageLayoutCallbackArgs\>) | يُستدعى هذا لإبلاغ عن تقدم بناء التخطيط وعرضه. |
| static [Type](./type/)() |  |
## ملاحظات


الاستخدام الأساسي لهذه الواجهة هو السماح لكود التطبيق بإلغاء عملية البناء.

يمكن بناء نموذج تخطيط الصفحة لعدد قليل فقط من الصفحات في بداية المستند ثم إلغاء العملية وعرض ما تم بناؤه بالفعل فقط.

مع ذلك، لاحظ أن نتائج العرض قد لا تتطابق مع ما كان سيُعرض لكل صفحة إذا انتهت العملية.

قد لا تعمل هذه التقنية مع كل مستند أو قد تفشل تمامًا.

## انظر أيضًا

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
