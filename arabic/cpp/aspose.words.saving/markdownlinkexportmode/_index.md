---
title: "Aspose::Words::Saving::MarkdownLinkExportMode enum"
linktitle: "MarkdownLinkExportMode"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::MarkdownLinkExportMode enum. يحدد كيفية تصدير الروابط إلى Markdown في C++."
type: docs
weight: 67000
url: /ar/cpp/aspose.words.saving/markdownlinkexportmode/
---
## MarkdownLinkExportMode enum


يحدد كيفية تصدير الروابط إلى Markdown.

```cpp
enum class MarkdownLinkExportMode
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| تلقائي | 0 | اكتشاف وضع التصدير تلقائيًا لكل رابط. |
| متضمن | 1 | تصدير جميع الروابط ككتل مضمنة. |
| مرجع | 2 | تصدير جميع الروابط ككتل مرجعية. |


## أمثلة



يظهر كيف سيتم كتابة الروابط إلى ملف .md.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertShape(Aspose::Words::Drawing::ShapeType::Balloon, 100, 100);

// سيتم كتابة الصورة كمرجع:
// ![ref1]
// [ref1]: aw_ref.001.png
auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_LinkExportMode(Aspose::Words::Saving::MarkdownLinkExportMode::Reference);
doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.LinkExportMode.Reference.md", saveOptions);

// سيتم كتابة الصورة كمدمجة:
// ![](aw_inline.001.png)
saveOptions->set_LinkExportMode(Aspose::Words::Saving::MarkdownLinkExportMode::Inline);
doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.LinkExportMode.Inline.md", saveOptions);
```

## انظر أيضًا

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
