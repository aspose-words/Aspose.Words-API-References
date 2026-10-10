---
title: "واجهة Aspose::Words::Saving::IFontSavingCallback"
linktitle: "IFontSavingCallback"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "واجهة Aspose::Words::Saving::IFontSavingCallback. نفّذ هذه الواجهة إذا كنت تريد تلقي الإشعارات والتحكم في طريقة حفظ Aspose.Words للخطوط عند تصدير مستند إلى تنسيق HTML في C++."
type: docs
weight: 42000
url: /ar/cpp/aspose.words.saving/ifontsavingcallback/
---
## IFontSavingCallback interface


قم بتنفيذ هذه الواجهة إذا كنت تريد تلقي الإشعارات والتحكم في طريقة حفظ Aspose.Words للخطوط عند تصدير مستند إلى تنسيق HTML.

```cpp
class IFontSavingCallback : public virtual System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| virtual [FontSaving](./fontsaving/)(System::SharedPtr\<Aspose::Words::Saving::FontSavingArgs\>) | يتم استدعاؤها عندما تكون Aspose.Words على وشك حفظ مورد الخط. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## انظر أيضًا

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
