---
title: "Aspose::Words::Saving::MarkdownListExportMode enum"
linktitle: "MarkdownListExportMode"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::MarkdownListExportMode enum. يحدد كيفية تصدير القوائم إلى Markdown بلغة C++."
type: docs
weight: 68000
url: /ar/cpp/aspose.words.saving/markdownlistexportmode/
---
## MarkdownListExportMode enum


يحدد كيفية تصدير القوائم إلى Markdown.

```cpp
enum class MarkdownListExportMode
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| MarkdownSyntax | 0 | تصدير عناصر القائمة المتوافقة مع صيغة Markdown. |
| نص عادي | 1 | تصدير عناصر القائمة كنص عادي. |


## أمثلة



يظهر كيف سيتم كتابة عناصر القائمة إلى مستند markdown.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List item.docx");

// استخدم MarkdownListExportMode.PlainText أو MarkdownListExportMode.MarkdownSyntax لتصدير القائمة.
auto options = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
options->set_ListExportMode(markdownListExportMode);
doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ListExportMode.md", options);
```

## انظر أيضًا

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
