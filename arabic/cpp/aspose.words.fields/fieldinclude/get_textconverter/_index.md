---
title: "طريقة Aspose::Words::Fields::FieldInclude::get_TextConverter"
linktitle: "get_TextConverter"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Fields::FieldInclude::get_TextConverter. يحصل أو يضبط اسم محول النص لتنسيق الملف المتضمن في C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words.fields/fieldinclude/get_textconverter/
---
## FieldInclude::get_TextConverter method


يحصل أو يعيّن اسم محوّل النص لتنسيق الملف المضمّن.

```cpp
System::String Aspose::Words::Fields::FieldInclude::get_TextConverter() override
```


## أمثلة



يظهر كيفية إنشاء حقل INCLUDE، وتعيين خصائصه.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// يمكننا استخدام حقل INCLUDE لاستيراد جزء من مستند آخر في نظام الملفات المحلي.
// الإشارة المرجعية من المستند الآخر التي نشير إليها بهذا الحقل تحتوي على هذا الجزء المستورد.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldInclude>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldInclude, true));
field->set_SourceFullName(get_MyDir() + u"Bookmarks.docx");
field->set_BookmarkName(u"MyBookmark1");
field->set_LockFields(false);
field->set_TextConverter(u"Microsoft Word");

ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(field->GetFieldCode(), u" INCLUDE .* MyBookmark1 \\\\c \"Microsoft Word\"")->get_Success());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INCLUDE.docx");
```

## انظر أيضًا

* Class [FieldInclude](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
