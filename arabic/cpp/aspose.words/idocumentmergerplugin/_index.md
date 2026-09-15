---
title: "Aspose::Words::IDocumentMergerPlugin interface"
linktitle: "IDocumentMergerPlugin"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "واجهة Aspose::Words::IDocumentMergerPlugin. تُعرّف واجهة للمكوّن الإضافي الخارجي للدمج الذي يمكنه دمج مستندات Pdf في C++."
type: docs
weight: 76500
url: /ar/cpp/aspose.words/idocumentmergerplugin/
---
## IDocumentMergerPlugin interface


يحدد واجهة لمكوّن دمج خارجي يمكنه دمج مستندات PDF.

```cpp
class IDocumentMergerPlugin : public virtual System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Merge](./merge/)(System::SharedPtr\<System::IO::Stream\>, System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>, System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\>) | يقوم بدمج مستندات PDF المدخلة المعطاة في مستند PDF واحد كخرج باستخدام تدفقات الإدخال والإخراج المحددة. |
| static [Type](./type/)() |  |
## انظر أيضًا

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
