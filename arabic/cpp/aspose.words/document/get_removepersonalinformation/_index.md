---
title: "طريقة Aspose::Words::Document::get_RemovePersonalInformation"
linktitle: "get_RemovePersonalInformation"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Document::get_RemovePersonalInformation. يحصل على أو يضبط علمًا يشير إلى أن Microsoft Word سيزيل جميع معلومات المستخدم من التعليقات، والتغييرات، وخصائص المستند عند حفظ المستند في C++."
type: docs
weight: 45000
url: /ar/cpp/aspose.words/document/get_removepersonalinformation/
---
## Document::get_RemovePersonalInformation method


يحصل على أو يضبط علامة تشير إلى أن Microsoft Word سيزيل جميع معلومات المستخدم من التعليقات والمراجعات وخصائص المستند عند حفظ المستند.

```cpp
bool Aspose::Words::Document::get_RemovePersonalInformation()
```


## أمثلة



يظهر كيفية تمكين إزالة المعلومات الشخصية أثناء حفظ يدوي.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// أدرج بعض المحتوى الذي يحتوي على معلومات شخصية.
doc->get_BuiltInDocumentProperties()->set_Author(u"John Doe");
doc->get_BuiltInDocumentProperties()->set_Company(u"Placeholder Inc.");

doc->StartTrackRevisions(doc->get_BuiltInDocumentProperties()->get_Author(), System::DateTime::get_Now());
builder->Write(u"Hello world!");
doc->StopTrackRevisions();

// هذا العلم يعادل File -> Options -> Trust Center -> Trust Center Settings... ->
// Privacy Options -> "Remove personal information from file properties on save" في Microsoft Word.
doc->set_RemovePersonalInformation(saveWithoutPersonalInfo);

// هذا الخيار لن يُطبق أثناء عملية حفظ تم إجراؤها باستخدام Aspose.Words.
// سيتم إزالة البيانات الشخصية من مستندنا عندما يكون العلم مفعلاً عند حفظه يدويًا باستخدام Microsoft Word.
doc->Save(get_ArtifactsDir() + u"Document.RemovePersonalInformation.docx");
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Document.RemovePersonalInformation.docx");

ASPOSE_ASSERT_EQ(saveWithoutPersonalInfo, doc->get_RemovePersonalInformation());
ASSERT_EQ(u"John Doe", doc->get_BuiltInDocumentProperties()->get_Author());
ASSERT_EQ(u"Placeholder Inc.", doc->get_BuiltInDocumentProperties()->get_Company());
ASSERT_EQ(u"John Doe", doc->get_Revisions()->idx_get(0)->get_Author());
```

## انظر أيضًا

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
