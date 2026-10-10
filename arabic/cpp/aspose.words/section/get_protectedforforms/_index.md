---
title: "طريقة Aspose::Words::Section::get_ProtectedForForms"
linktitle: "get_ProtectedForForms"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Section::get_ProtectedForForms. صحيح إذا كان القسم محميًا للنماذج. عندما يكون القسم محميًا للنماذج، يمكن للمستخدمين تحديد وتعديل النص فقط في حقول النموذج في Microsoft Word في C++."
type: docs
weight: 14000
url: /ar/cpp/aspose.words/section/get_protectedforforms/
---
## Section::get_ProtectedForForms method


صحيح إذا كان القسم محمياً للنماذج. عندما يكون القسم محمياً للنماذج، يمكن للمستخدمين تحديد النص وتعديله فقط في حقول النماذج في Microsoft Word.

```cpp
bool Aspose::Words::Section::get_ProtectedForForms()
```


## أمثلة



يظهر كيفية إيقاف الحماية لقسم.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Section 1. Hello world!");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);

builder->Writeln(u"Section 2. Hello again!");
builder->Write(u"Please enter text here: ");
builder->InsertTextInput(u"TextInput1", Aspose::Words::Fields::TextFormFieldType::Regular, u"", u"Placeholder text", 0);

// تطبيق حماية كتابة على كل قسم في المستند.
doc->Protect(Aspose::Words::ProtectionType::AllowOnlyFormFields);

// إيقاف حماية الكتابة للقسم الأول.
doc->get_Sections()->idx_get(0)->set_ProtectedForForms(false);

// في مستند الإخراج هذا، سنتمكن من تحرير القسم الأول بحرية،
// وسنتمكن فقط من تحرير محتويات حقل النموذج في القسم الثاني.
doc->Save(get_ArtifactsDir() + u"Section.Protect.docx");
```

## انظر أيضًا

* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
