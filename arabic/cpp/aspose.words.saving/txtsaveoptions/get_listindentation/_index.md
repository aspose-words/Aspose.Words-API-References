---
title: "طريقة Aspose::Words::Saving::TxtSaveOptions::get_ListIndentation"
linktitle: "get_ListIndentation"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::TxtSaveOptions::get_ListIndentation. يحصل على كائن TxtListIndentation يحدد عدد وحرف الإزاحة لاستخدامه في مستويات القوائم. بشكل افتراضي، يكون عدد الأحرف ''\\\\0'' صفرًا، مما يعني عدم وجود إزاحة في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words.saving/txtsaveoptions/get_listindentation/
---
## TxtSaveOptions::get_ListIndentation method


يحصل على كائن [TxtListIndentation](../../txtlistindentation/) يحدد عدد وحرف الإزاحة لاستخدامه في مستويات القوائم. بشكل افتراضي، يكون عدد الأحرف '\\0' صفرًا، مما يعني عدم وجود إزاحة.

```cpp
System::SharedPtr<Aspose::Words::Saving::TxtListIndentation> Aspose::Words::Saving::TxtSaveOptions::get_ListIndentation() const
```


## أمثلة



يعرض كيفية تكوين إزاحة القوائم عند حفظ المستند كنص عادي.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// إنشاء قائمة بثلاث مستويات من الإزاحة.
builder->get_ListFormat()->ApplyNumberDefault();
builder->Writeln(u"Item 1");
builder->get_ListFormat()->ListIndent();
builder->Writeln(u"Item 2");
builder->get_ListFormat()->ListIndent();
builder->Write(u"Item 3");

// إنشاء كائن "TxtSaveOptions"، والذي يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
// لتعديل طريقة حفظ المستند كنص عادي.
auto txtSaveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();

// قم بتعيين خاصية \"Character\" لتحديد حرف لاستخدامه
// للتعبئة التي تحاكي إزاحة القوائم في النص العادي.
txtSaveOptions->get_ListIndentation()->set_Character(u' ');

// قم بتعيين خاصية \"Count\" لتحديد عدد المرات
// لوضع حرف التعبئة لكل مستوى إزاحة قائمة.
txtSaveOptions->get_ListIndentation()->set_Count(3);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.TxtListIndentation.txt", txtSaveOptions);

System::String docText = System::IO::File::ReadAllText(get_ArtifactsDir() + u"TxtSaveOptions.TxtListIndentation.txt");
System::String newLine = System::Environment::get_NewLine();

ASSERT_EQ(System::String::Format(u"1. Item 1{0}", newLine) + System::String::Format(u"   a. Item 2{0}", newLine) + System::String::Format(u"      i. Item 3{0}", newLine), docText);
```

## انظر أيضًا

* Class [TxtListIndentation](../../txtlistindentation/)
* Class [TxtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
