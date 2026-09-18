---
title: "Aspose::Words::Loading::MarkdownLoadOptions::get_ImportUnderlineFormatting Methode"
linktitle: "get_ImportUnderlineFormatting"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Loading::MarkdownLoadOptions::get_ImportUnderlineFormatting Methode. Gibt einen booleschen Wert zurück oder setzt ihn, der angibt, ob eine Sequenz von zwei Pluszeichen \\\"++\\\" als Unterstreichungs-Textformatierung erkannt werden soll. Der Standardwert ist false in C++."
type: docs
weight: 3000
url: /de/cpp/aspose.words.loading/markdownloadoptions/get_importunderlineformatting/
---
## MarkdownLoadOptions::get_ImportUnderlineFormatting method


Liest oder setzt einen booleschen Wert, der angibt, ob eine Sequenz von zwei Pluszeichen "++" als Unterstreichungs-Textformatierung erkannt werden soll. Der Standardwert ist **false**.

```cpp
bool Aspose::Words::Loading::MarkdownLoadOptions::get_ImportUnderlineFormatting() const
```


## Beispiele



Zeigt, wie man Pluszeichen \"++\" als Unterstreichungs-Textformatierung erkennt.
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

## Siehe auch

* Class [MarkdownLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
