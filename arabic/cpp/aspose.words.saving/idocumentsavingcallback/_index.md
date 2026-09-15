---
title: "واجهة Aspose::Words::Saving::IDocumentSavingCallback"
linktitle: "IDocumentSavingCallback"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "واجهة Aspose::Words::Saving::IDocumentSavingCallback. نفّذ هذه الواجهة إذا كنت تريد أن يكون لديك طريقة مخصصة تُستدعى أثناء حفظ مستند في C++."
type: docs
weight: 41000
url: /ar/cpp/aspose.words.saving/idocumentsavingcallback/
---
## IDocumentSavingCallback interface


قم بتنفيذ هذه الواجهة إذا كنت تريد امتلاك طريقة مخصصة خاصة بك تُستدعى أثناء حفظ المستند.

```cpp
class IDocumentSavingCallback : public virtual System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Notify](./notify/)(System::SharedPtr\<Aspose::Words::Saving::DocumentSavingArgs\>) | يتم استدعاؤها لإبلاغ عن تقدم حفظ المستند. |
| static [Type](./type/)() |  |
## انظر أيضًا

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
