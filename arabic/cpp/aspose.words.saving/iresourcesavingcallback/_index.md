---
title: "Aspose::Words::Saving::IResourceSavingCallback interface"
linktitle: "IResourceSavingCallback"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::IResourceSavingCallback interface. نفّذ هذه الواجهة إذا كنت تريد التحكم في كيفية حفظ Aspose.Words للموارد الخارجية (الصور، الخطوط و css) عند حفظ مستند إلى HTML ثابت أو SVG في C++."
type: docs
weight: 45000
url: /ar/cpp/aspose.words.saving/iresourcesavingcallback/
---
## IResourceSavingCallback interface


قم بتنفيذ هذه الواجهة إذا كنت تريد التحكم في طريقة حفظ Aspose.Words للموارد الخارجية (الصور، الخطوط و css) عند حفظ مستند إلى HTML ثابت أو SVG.

```cpp
class IResourceSavingCallback : public virtual System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [ResourceSaving](./resourcesaving/)(System::SharedPtr\<Aspose::Words::Saving::ResourceSavingArgs\>) | يُستدعى عندما تقوم Aspose.Words بحفظ مورد خارجي إلى تنسيقات HTML ثابت أو SVG. |
| static [Type](./type/)() |  |
## انظر أيضًا

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
