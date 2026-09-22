---
title: "طريقة Aspose::Words::Saving::MarkdownSaveOptions::get_ExportAsHtml"
linktitle: "get_ExportAsHtml"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::MarkdownSaveOptions::get_ExportAsHtml. يسمح بتحديد العناصر التي سيتم تصديرها إلى Markdown كـ HTML خام. القيمة الافتراضية هي None في C++."
type: docs
weight: 2500
url: /ar/cpp/aspose.words.saving/markdownsaveoptions/get_exportashtml/
---
## MarkdownSaveOptions::get_ExportAsHtml method


يسمح بتحديد العناصر التي سيتم تصديرها إلى Markdown كـ HTML خام. القيمة الافتراضية هي [None](../../markdownexportashtml/).

```cpp
Aspose::Words::Saving::MarkdownExportAsHtml Aspose::Words::Saving::MarkdownSaveOptions::get_ExportAsHtml() const
```


## أمثلة



يوضح كيفية تصدير جدول إلى Markdown كـ HTML خام.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Sample table:");

// إنشاء جدول.
builder->InsertCell();
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Right);
builder->Write(u"Cell1");
builder->InsertCell();
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
builder->Write(u"Cell2");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_ExportAsHtml(Aspose::Words::Saving::MarkdownExportAsHtml::Tables);

doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ExportTableAsHtml.md", saveOptions);
```

## انظر أيضًا

* Enum [MarkdownExportAsHtml](../../markdownexportashtml/)
* Class [MarkdownSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
