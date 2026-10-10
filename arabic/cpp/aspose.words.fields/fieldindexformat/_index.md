---
title: "Aspose::Words::Fields::FieldIndexFormat تعداد"
linktitle: "FieldIndexFormat"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fields::FieldIndexFormat تعداد. يحدد تنسيق حقول FieldIndex في مستند بلغة C++."
type: docs
weight: 129000
url: /ar/cpp/aspose.words.fields/fieldindexformat/
---
## FieldIndexFormat enum


يحدد تنسيق حقول [FieldIndex](../fieldindex/) في مستند.

```cpp
enum class FieldIndexFormat
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| قالب | 0 | من القالب. |
| كلاسيكي | 1 | كلاسيكي. |
| فاخر | 2 | فاخر. |
| حديث | 3 | حديث. |
| مرقّم | 4 | مرقّم. |
| رسمي | 5 | رسمي. |
| بسيط | 6 | بسيط. |


## أمثلة



يظهر كيفية تنسيق حقول [FieldIndex](../fieldindex/).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"A");
builder->InsertBreak(Aspose::Words::BreakType::LineBreak);
builder->InsertField(u"XE \"A\"");
builder->Write(u"B");

builder->InsertField(u" INDEX \\e \" · \" \\h \"A\" \\c \"2\" \\z \"1033\"", nullptr);

doc->get_FieldOptions()->set_FieldIndexFormat(Aspose::Words::Fields::FieldIndexFormat::Fancy);
doc->UpdateFields();

doc->Save(get_ArtifactsDir() + u"Field.SetFieldIndexFormat.docx");
```

## انظر أيضًا

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
