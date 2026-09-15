---
title: "Aspose::Words::Saving::MarkdownExportAsHtml enum"
linktitle: "MarkdownExportAsHtml"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "تعداد Aspose::Words::Saving::MarkdownExportAsHtml. يسمح بتحديد العناصر التي سيتم تصديرها إلى Markdown كـ HTML خام في C++."
type: docs
weight: 66500
url: /ar/cpp/aspose.words.saving/markdownexportashtml/
---
## MarkdownExportAsHtml enum


يسمح بتحديد العناصر التي سيتم تصديرها إلى Markdown كـ HTML خام.

```cpp
enum class MarkdownExportAsHtml
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| None | 0 | صدّر جميع العناصر باستخدام صيغة Markdown دون أي HTML خام. |
| الجداول | 1 | تصدير الجداول كـ HTML خام. |
| NonCompatibleTables | 2 | تصدير الجداول التي لا يمكن تمثيلها بشكل صحيح في Markdown النقي كـ HTML خام. |


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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
