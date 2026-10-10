---
title: "Aspose::Words::Fields::FieldIncludePicture::get_ResizeHorizontally طريقة"
linktitle: "get_ResizeHorizontally"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fields::FieldIncludePicture::get_ResizeHorizontally طريقة. يحصل أو يضبط ما إذا كان يجب تغيير حجم الصورة أفقياً من المصدر في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words.fields/fieldincludepicture/get_resizehorizontally/
---
## FieldIncludePicture::get_ResizeHorizontally method


يحصل أو يضبط ما إذا كان سيتم تغيير حجم الصورة أفقياً من المصدر.

```cpp
bool Aspose::Words::Fields::FieldIncludePicture::get_ResizeHorizontally()
```


## أمثلة



يعرض كيفية إدراج الصور باستخدام حقول IMPORT و INCLUDEPICTURE.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// فيما يلي نوعان من الحقول المتشابهة يمكننا استخدامها لعرض الصور المرتبطة من نظام الملفات المحلي.
// 1 -  حقل INCLUDEPICTURE:
auto fieldIncludePicture = System::ExplicitCast<Aspose::Words::Fields::FieldIncludePicture>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIncludePicture, true));
fieldIncludePicture->set_SourceFullName(get_ImageDir() + u"Transparent background logo.png");

ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(fieldIncludePicture->GetFieldCode(), u" INCLUDEPICTURE  .*")->get_Success());

// قم بتطبيق مرشح PNG32.FLT.
fieldIncludePicture->set_GraphicFilter(u"PNG32");
fieldIncludePicture->set_IsLinked(true);
fieldIncludePicture->set_ResizeHorizontally(true);
fieldIncludePicture->set_ResizeVertically(true);

// 2 -  حقل IMPORT:
auto fieldImport = System::ExplicitCast<Aspose::Words::Fields::FieldImport>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldImport, true));
fieldImport->set_SourceFullName(get_ImageDir() + u"Transparent background logo.png");
fieldImport->set_GraphicFilter(u"PNG32");
fieldImport->set_IsLinked(true);

ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(fieldImport->GetFieldCode(), u" IMPORT  .* \\\\c PNG32 \\\\d")->get_Success());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.IMPORT.INCLUDEPICTURE.docx");
```

## انظر أيضًا

* Class [FieldIncludePicture](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
