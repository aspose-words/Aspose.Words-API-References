---
title: "Aspose::Words::Loading::MarkdownLoadOptions::get_ImportUnderlineFormatting metod"
linktitle: "get_ImportUnderlineFormatting"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Loading::MarkdownLoadOptions::get_ImportUnderlineFormatting metod. Hämtar eller anger ett booleskt värde som indikerar om en sekvens av två plustecken \"++\" ska kännas igen som understruken textformatering. Standardvärdet är falskt i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words.loading/markdownloadoptions/get_importunderlineformatting/
---
## MarkdownLoadOptions::get_ImportUnderlineFormatting method


Hämtar eller anger ett booleskt värde som indikerar om en sekvens av två plustecken "++" ska kännas som understruken textformatering. Standardvärdet är **false**.

```cpp
bool Aspose::Words::Loading::MarkdownLoadOptions::get_ImportUnderlineFormatting() const
```


## Exempel



Visar hur man känner igen plustecknen "++" som understruken textformatering.
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

## Se även

* Class [MarkdownLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
