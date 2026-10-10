---
title: "Aspose::Words::Saving::MarkdownEmptyParagraphExportMode enum"
linktitle: "MarkdownEmptyParagraphExportMode"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::MarkdownEmptyParagraphExportMode enum. يحدد كيفية تصدير Aspose.Words للفقرات الفارغة إلى Markdown في C++."
type: docs
weight: 66250
url: /ar/cpp/aspose.words.saving/markdownemptyparagraphexportmode/
---
## MarkdownEmptyParagraphExportMode enum


يحدد كيفية تصدير Aspose.Words للفقرات الفارغة إلى Markdown.

```cpp
enum class MarkdownEmptyParagraphExportMode
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| EmptyLine | 0 | تصدير كخطوط فارغة. |
| MarkdownHardLineBreak | 1 | تصدير كحرف Markdown HardLineBreak '\'. |
| None | 2 | لا تقم بتصدير الفقرات الفارغة. |


## أمثلة



يعرض كيفية تصدير الفقرات الفارغة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"First");
builder->Writeln(u"\r\n\r\n\r\n");
builder->Writeln(u"Last");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_EmptyParagraphExportMode(exportMode);

doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.EmptyParagraphExportMode.md", saveOptions);

System::String result = System::IO::File::ReadAllText(get_ArtifactsDir() + u"MarkdownSaveOptions.EmptyParagraphExportMode.md");

switch (exportMode)
{
    case Aspose::Words::Saving::MarkdownEmptyParagraphExportMode::None:
        ASSERT_EQ(u"First\r\n\r\nLast\r\n", result);
        break;

    case Aspose::Words::Saving::MarkdownEmptyParagraphExportMode::EmptyLine:
        ASSERT_EQ(u"First\r\n\r\n\r\n\r\n\r\nLast\r\n\r\n", result);
        break;

    case Aspose::Words::Saving::MarkdownEmptyParagraphExportMode::MarkdownHardLineBreak:
        ASSERT_EQ(u"First\r\n\\\r\n\\\r\n\\\r\n\\\r\n\\\r\nLast\r\n<br>\r\n", result);
        break;

}
```

## انظر أيضًا

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
