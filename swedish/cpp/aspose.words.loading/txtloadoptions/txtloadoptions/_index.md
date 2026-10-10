---
title: "Aspose::Words::Loading::TxtLoadOptions::TxtLoadOptions konstruktor"
linktitle: "TxtLoadOptions"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Loading::TxtLoadOptions::TxtLoadOptions konstruktor. Initierar en ny instans av denna klass med standardvärden i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.loading/txtloadoptions/txtloadoptions/
---
## TxtLoadOptions::TxtLoadOptions constructor


Initierar en ny instans av den här klassen med standardvärden.

```cpp
Aspose::Words::Loading::TxtLoadOptions::TxtLoadOptions()
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
