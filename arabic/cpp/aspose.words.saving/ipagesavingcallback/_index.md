---
title: "واجهة Aspose::Words::Saving::IPageSavingCallback"
linktitle: "IPageSavingCallback"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "واجهة Aspose::Words::Saving::IPageSavingCallback. نفّذ هذه الواجهة إذا أردت التحكم في طريقة حفظ Aspose.Words للصفحات المنفصلة عند حفظ المستند بتنسيقات الصفحات الثابتة في C++."
type: docs
weight: 44000
url: /ar/cpp/aspose.words.saving/ipagesavingcallback/
---
## IPageSavingCallback interface


قم بتنفيذ هذه الواجهة إذا كنت تريد التحكم في طريقة حفظ Aspose.Words للصفحات المنفصلة عند حفظ مستند إلى تنسيقات صفحات ثابتة.

```cpp
class IPageSavingCallback : public virtual System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [PageSaving](./pagesaving/)(System::SharedPtr\<Aspose::Words::Saving::PageSavingArgs\>) | يتم استدعاؤها عندما يقوم Aspose.Words بحفظ صفحة منفصلة إلى تنسيقات الصفحات الثابتة. |
| static [Type](./type/)() |  |
## انظر أيضًا

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
