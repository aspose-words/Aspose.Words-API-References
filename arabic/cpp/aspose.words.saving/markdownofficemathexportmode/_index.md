---
title: "تعداد Aspose::Words::Saving::MarkdownOfficeMathExportMode"
linktitle: "MarkdownOfficeMathExportMode"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "تعداد Aspose::Words::Saving::MarkdownOfficeMathExportMode. يحدد كيفية تصدير Aspose.Words لـ OfficeMath إلى Markdown في C++."
type: docs
weight: 68500
url: /ar/cpp/aspose.words.saving/markdownofficemathexportmode/
---
## MarkdownOfficeMathExportMode enum


يحدد كيفية تصدير Aspose.Words لـ OfficeMath إلى Markdown.

```cpp
enum class MarkdownOfficeMathExportMode
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| Text | 0 | تصدير OfficeMath كنص عادي. |
| Image | 1 | تصدير OfficeMath كصورة. |
| MathML | 2 | تصدير OfficeMath كـ MathML. |
| Latex | 3 | تصدير OfficeMath كـ LaTeX. |
| MarkItDown | 4 | تصدير OfficeMath كـ LaTeX متوافق مع MarkItDown. |


## أمثلة



يظهر كيف سيتم كتابة OfficeMath إلى المستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_OfficeMathExportMode(Aspose::Words::Saving::MarkdownOfficeMathExportMode::Image);

doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.OfficeMathExportMode.md", saveOptions);
```


يظهر كيفية تصدير كائن OfficeMath كـ Latex.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_OfficeMathExportMode(Aspose::Words::Saving::MarkdownOfficeMathExportMode::Latex);

doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ExportOfficeMathAsLatex.md", saveOptions);
```


يظهر كيفية تصدير كائن OfficeMath كـ MarkItDown.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_OfficeMathExportMode(Aspose::Words::Saving::MarkdownOfficeMathExportMode::MarkItDown);

doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ExportOfficeMathAsMarkItDown.md", saveOptions);
```

## انظر أيضًا

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
