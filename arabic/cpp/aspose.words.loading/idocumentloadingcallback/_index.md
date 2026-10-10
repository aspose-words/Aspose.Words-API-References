---
title: "واجهة Aspose::Words::Loading::IDocumentLoadingCallback"
linktitle: "IDocumentLoadingCallback"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "واجهة Aspose::Words::Loading::IDocumentLoadingCallback. نفّذ هذه الواجهة إذا كنت تريد أن يكون لديك طريقتك المخصصة التي تُستدعى أثناء تحميل مستند في C++."
type: docs
weight: 10000
url: /ar/cpp/aspose.words.loading/idocumentloadingcallback/
---
## IDocumentLoadingCallback interface


نفّذ هذه الواجهة إذا كنت ترغب في وجود طريقة مخصصة خاصة بك تُستدعى أثناء تحميل المستند.

```cpp
class IDocumentLoadingCallback : public virtual System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Notify](./notify/)(System::SharedPtr\<Aspose::Words::Loading::DocumentLoadingArgs\>) | يُستدعى هذا لإبلاغ عن تقدم تحميل المستند. |
| static [Type](./type/)() |  |
## انظر أيضًا

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
