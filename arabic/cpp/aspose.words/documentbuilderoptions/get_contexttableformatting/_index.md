---
title: "طريقة Aspose::Words::DocumentBuilderOptions::get_ContextTableFormatting"
linktitle: "get_ContextTableFormatting"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::DocumentBuilderOptions::get_ContextTableFormatting. صحيح إذا كان التنسيق المطبق على محتوى الجدول لا يؤثر على تنسيق المحتوى الذي يليه. القيمة الافتراضية هي true في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words/documentbuilderoptions/get_contexttableformatting/
---
## DocumentBuilderOptions::get_ContextTableFormatting method


صحيح إذا كان التنسيق المطبق على محتوى الجدول لا يؤثر على تنسيق المحتوى الذي يليه. القيمة الافتراضية هي **true**.

```cpp
bool Aspose::Words::DocumentBuilderOptions::get_ContextTableFormatting() const
```


## أمثلة



يعرض كيفية تجاهل تنسيق الجدول للمحتوى التالي.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builderOptions = System::MakeObject<Aspose::Words::DocumentBuilderOptions>();
builderOptions->set_ContextTableFormatting(true);
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc, builderOptions);

// يضيف محتوى قبل الجدول.
// حجم الخط الافتراضي هو 12.
builder->Writeln(u"Font size 12 here.");
builder->StartTable();
builder->InsertCell();
// يغيّر حجم الخط داخل الجدول.
builder->get_Font()->set_Size(5);
builder->Write(u"Font size 5 here");
builder->InsertCell();
builder->Write(u"Font size 5 here");
builder->EndRow();
builder->EndTable();

// إذا كان ContextTableFormatting صحيحًا، فإن تنسيق الجدول لا يُطبق على المحتوى التالي.
// إذا كان ContextTableFormatting خاطئًا، فإن تنسيق الجدول يُطبق على المحتوى التالي.
builder->Writeln(u"Font size 12 here.");

doc->Save(get_ArtifactsDir() + u"Table.ContextTableFormatting.docx");
```

## انظر أيضًا

* Class [DocumentBuilderOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
