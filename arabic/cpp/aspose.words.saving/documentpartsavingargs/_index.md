---
title: "فئة Aspose::Words::Saving::DocumentPartSavingArgs"
linktitle: "DocumentPartSavingArgs"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::Saving::DocumentPartSavingArgs. توفر بيانات لاستدعاء DocumentPartSaving(). لمعرفة المزيد، قم بزيارة مقالة الوثائق في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words.saving/documentpartsavingargs/
---
## DocumentPartSavingArgs class


توفر بيانات لاستدعاء [DocumentPartSaving()](../idocumentpartsavingcallback/documentpartsaving/). لمعرفة المزيد، قم بزيارة مقالة الوثائق [Save a Document](https://docs.aspose.com/words/cpp/save-a-document/).

```cpp
class DocumentPartSavingArgs : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_Document](./get_document/)() const | يحصل على كائن المستند الذي يتم حفظه. |
| [get_DocumentPartFileName](./get_documentpartfilename/)() const | يحصل أو يعيّن اسم الملف (بدون المسار) حيث سيتم حفظ جزء المستند. |
| [get_DocumentPartStream](./get_documentpartstream/)() const | يسمح بتحديد الدفق حيث سيتم حفظ جزء المستند. |
| [get_KeepDocumentPartStreamOpen](./get_keepdocumentpartstreamopen/)() const | يحدد ما إذا كان يجب على Aspose.Words إبقاء الدفق مفتوحًا أو إغلاقه بعد حفظ جزء المستند. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_DocumentPartFileName](./set_documentpartfilename/)(const System::String\&) | معين لـ [Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartFileName](./get_documentpartfilename/). |
| [set_DocumentPartStream](./set_documentpartstream/)(const System::SharedPtr\<System::IO::Stream\>\&) | معين لـ [Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartStream](./get_documentpartstream/). |
| [set_DocumentPartStream](./set_documentpartstream/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| [set_KeepDocumentPartStreamOpen](./set_keepdocumentpartstreamopen/)(bool) | معين لـ [Aspose::Words::Saving::DocumentPartSavingArgs::get_KeepDocumentPartStreamOpen](./get_keepdocumentpartstreamopen/). |
| static [Type](./type/)() |  |
## ملاحظات


عند حفظ Aspose.Words لمستند إلى HTML أو صيغ ذات صلة وتحديد [DocumentSplitCriteria](../htmlsaveoptions/get_documentsplitcriteria/)، يتم تقسيم المستند إلى أجزاء وبشكل افتراضي، يتم حفظ كل جزء من المستند في ملف منفصل.

الفئة [DocumentPartSavingArgs](./) تتيح لك التحكم في كيفية حفظ كل جزء من المستند. تسمح بإعادة تعريف كيفية إنشاء أسماء الملفات أو لتجاوز حفظ أجزاء المستند في ملفات تمامًا عن طريق توفير كائنات الدفق الخاصة بك.

لحفظ أجزاء المستند في الدفقات بدلاً من الملفات، استخدم الخاصية [DocumentPartStream](./get_documentpartstream/).
## انظر أيضًا

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
