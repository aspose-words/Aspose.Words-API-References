---
title: "تعداد Aspose::Words::ProtectionType"
linktitle: "ProtectionType"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "تعداد Aspose::Words::ProtectionType. نوع الحماية لمستند في C++."
type: docs
weight: 111000
url: /ar/cpp/aspose.words/protectiontype/
---
## ProtectionType enum


نوع الحماية للمستند.

```cpp
enum class ProtectionType
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| AllowOnlyComments | 1 | يمكن للمستخدم تعديل التعليقات فقط في المستند. |
| AllowOnlyFormFields | 2 | يمكن للمستخدم إدخال البيانات فقط في حقول النموذج في المستند. |
| AllowOnlyRevisions | 0 | يمكن للمستخدم إضافة علامات المراجعة فقط إلى المستند. |
| ReadOnly | 3 | لا يُسمح بأي تغييرات على المستند. متاح منذ Microsoft Word 2003. |
| NoProtection | -1 | المستند غير محمي. |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
