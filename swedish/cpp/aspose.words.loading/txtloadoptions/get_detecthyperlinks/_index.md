---
title: "Aspose::Words::Loading::TxtLoadOptions::get_DetectHyperlinks-metod"
linktitle: "get_DetectHyperlinks"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Loading::TxtLoadOptions::get_DetectHyperlinks-metod. Anger om hyperlänkar ska detekteras i texten. Standardvärdet är false i C++."
type: docs
weight: 3500
url: /sv/cpp/aspose.words.loading/txtloadoptions/get_detecthyperlinks/
---
## TxtLoadOptions::get_DetectHyperlinks method


Anger om hyperlänkar ska detekteras i text. Standardvärdet är **false**.

```cpp
bool Aspose::Words::Loading::TxtLoadOptions::get_DetectHyperlinks() const
```


## Exempel



Visar hur man läser och visar hyperlänkar.
```cpp
const System::String inputText = System::String(u"Some links in TXT:\n") + u"https://www.aspose.com/\n" + u"https://docs.aspose.com/words/net/\n";

{
    System::SharedPtr<System::IO::Stream> stream = System::MakeObject<System::IO::MemoryStream>();
    System::ArrayPtr<uint8_t> buf = System::Text::Encoding::get_ASCII()->GetBytes(inputText);
    stream->Write(buf, 0, buf->get_Length());
    auto loadOptions = System::MakeObject<Aspose::Words::Loading::TxtLoadOptions>();
    loadOptions->set_DetectHyperlinks(true);

    // Läs in dokument med hyperlänkar.
    auto doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);

    // Skriv ut hyperlänkt text.
    for (auto&& field : System::IterateOver(doc->get_Range()->get_Fields()))
    {
        std::cout << field->get_Result() << std::endl;
    }

    ASSERT_EQ(doc->get_Range()->get_Fields()->idx_get(0)->get_Result().Trim(), u"https://www.aspose.com/");
    ASSERT_EQ(doc->get_Range()->get_Fields()->idx_get(1)->get_Result().Trim(), u"https://docs.aspose.com/words/net/");
}
```

## Se även

* Class [TxtLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
