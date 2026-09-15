---
title: "Aspose::Words::Saving::IDocumentPartSavingCallback interface"
linktitle: "IDocumentPartSavingCallback"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "واجهة Aspose::Words::Saving::IDocumentPartSavingCallback. نفّذ هذه الواجهة إذا كنت ترغب في تلقي الإشعارات والتحكم في كيفية حفظ Aspose.Words لأجزاء المستند عند تصدير المستند إلى تنسيق Html أو Epub في C++."
type: docs
weight: 40000
url: /ar/cpp/aspose.words.saving/idocumentpartsavingcallback/
---
## IDocumentPartSavingCallback interface


نفّذ هذه الواجهة إذا كنت ترغب في تلقي الإشعارات والتحكم في كيفية حفظ Aspose.Words لأجزاء المستند عند تصدير المستند إلى تنسيق [Html](../../aspose.words/saveformat/) أو [Epub](../../aspose.words/saveformat/).

```cpp
class IDocumentPartSavingCallback : public virtual System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| virtual [DocumentPartSaving](./documentpartsaving/)(System::SharedPtr\<Aspose::Words::Saving::DocumentPartSavingArgs\>) | يُستدعى عندما يكون Aspose.Words على وشك حفظ جزء من المستند. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## انظر أيضًا

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
