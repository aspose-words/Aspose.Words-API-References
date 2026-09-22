---
title: "الواجهة Aspose::Words::Saving::ICssSavingCallback"
linktitle: "ICssSavingCallback"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "الواجهة Aspose::Words::Saving::ICssSavingCallback. نفّذ هذه الواجهة إذا كنت تريد التحكم في طريقة حفظ Aspose.Words لملفات CSS (Cascading Style Sheet) عند حفظ مستند إلى HTML في C++."
type: docs
weight: 39000
url: /ar/cpp/aspose.words.saving/icsssavingcallback/
---
## ICssSavingCallback interface


نفّذ هذه الواجهة إذا كنت تريد التحكم في طريقة حفظ Aspose.Words لملفات CSS (Cascading [Style](../../aspose.words/style/) Sheet) عند حفظ مستند إلى HTML.

```cpp
class ICssSavingCallback : public virtual System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| virtual [CssSaving](./csssaving/)(System::SharedPtr\<Aspose::Words::Saving::CssSavingArgs\>) | يتم الاستدعاء عندما يقوم Aspose.Words بحفظ CSS (Cascading [Style](../../aspose.words/style/) Sheet). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## انظر أيضًا

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
