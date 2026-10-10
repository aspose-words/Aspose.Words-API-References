---
title: "Aspose::Words::Loading::MarkdownLoadOptions::get_ImportUnderlineFormatting طريقة"
linktitle: "set_ImportUnderlineFormatting"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Loading::MarkdownLoadOptions::get_ImportUnderlineFormatting طريقة. يحصل أو يعيّن قيمة منطقية تشير إلى ما إذا كان يجب التعرف على تسلسل من حرفين زائد \"++\" كتنسيق نص تحتي. القيمة الافتراضية هي false في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.loading/markdownloadoptions/get_importunderlineformatting/
---
## MarkdownLoadOptions::get_ImportUnderlineFormatting method


يحصل أو يعيّن قيمة منطقية تشير إلى ما إذا كان يجب التعرف على تسلسل من حرفي زائد "++" كتنسيق نص تحتي. القيمة الافتراضية هي **false**.

```cpp
bool Aspose::Words::Loading::MarkdownLoadOptions::get_ImportUnderlineFormatting() const
```


## أمثلة



يعرض كيفية التعرف على أحرف الزائد "++" كتنسيق نص تحتي.
```cpp
{
    auto stream = System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_ASCII()->GetBytes(u"++12 and B++"));
    auto loadOptions = System::MakeObject<Aspose::Words::Loading::MarkdownLoadOptions>();
    loadOptions->set_ImportUnderlineFormatting(true);
    auto doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);

    auto para = System::ExplicitCast<Aspose::Words::Paragraph>(doc->GetChild(Aspose::Words::NodeType::Paragraph, 0, true));
    ASSERT_EQ(Aspose::Words::Underline::Single, para->get_Runs()->idx_get(0)->get_Font()->get_Underline());

    loadOptions = System::MakeObject<Aspose::Words::Loading::MarkdownLoadOptions>();
    loadOptions->set_ImportUnderlineFormatting(false);
    doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);

    para = System::ExplicitCast<Aspose::Words::Paragraph>(doc->GetChild(Aspose::Words::NodeType::Paragraph, 0, true));
    ASSERT_EQ(Aspose::Words::Underline::None, para->get_Runs()->idx_get(0)->get_Font()->get_Underline());
}
```

## انظر أيضًا

* Class [MarkdownLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
