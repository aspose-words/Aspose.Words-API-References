---
title: "واجهة Aspose::Words::Saving::IImageSavingCallback"
linktitle: "IImageSavingCallback"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "واجهة Aspose::Words::Saving::IImageSavingCallback. نفّذ هذه الواجهة إذا كنت تريد التحكم في طريقة حفظ Aspose.Words للصور عند حفظ مستند إلى HTML. قد تُستخدم من قبل صيغ أخرى في C++."
type: docs
weight: 43000
url: /ar/cpp/aspose.words.saving/iimagesavingcallback/
---
## IImageSavingCallback interface


قم بتنفيذ هذه الواجهة إذا كنت تريد التحكم في طريقة حفظ Aspose.Words للصور عند حفظ مستند إلى HTML. قد يُستخدم بواسطة تنسيقات أخرى.

```cpp
class IImageSavingCallback : public virtual System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| virtual [ImageSaving](./imagesaving/)(System::SharedPtr\<Aspose::Words::Saving::ImageSavingArgs\>) | تُستدعى عندما يقوم Aspose.Words بحفظ صورة إلى HTML. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## انظر أيضًا

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
