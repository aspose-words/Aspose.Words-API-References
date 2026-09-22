---
title: "Aspose::Words::Loading::IResourceLoadingCallback interface"
linktitle: "IResourceLoadingCallback"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Loading::IResourceLoadingCallback interface. نفّذ هذه الواجهة إذا كنت ترغب في التحكم في طريقة تحميل Aspose.Words للموارد الخارجية عند استيراد مستند وإدراج صور باستخدام DocumentBuilder في C++."
type: docs
weight: 11000
url: /ar/cpp/aspose.words.loading/iresourceloadingcallback/
---
## IResourceLoadingCallback interface


نفّذ هذه الواجهة إذا كنت ترغب في التحكم في طريقة تحميل Aspose.Words للموارد الخارجية عند إدراج صور باستخدام [DocumentBuilder](../../aspose.words/documentbuilder/).

```cpp
class IResourceLoadingCallback : public virtual System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [ResourceLoading](./resourceloading/)(System::SharedPtr\<Aspose::Words::Loading::ResourceLoadingArgs\>) | يتم استدعاؤها عندما يقوم Aspose.Words بتحميل أي مورد خارجي. |
| static [Type](./type/)() |  |
## انظر أيضًا

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
