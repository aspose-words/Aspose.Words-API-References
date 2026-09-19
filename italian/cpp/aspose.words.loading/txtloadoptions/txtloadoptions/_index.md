---
title: "Costruttore Aspose::Words::Loading::TxtLoadOptions::TxtLoadOptions"
linktitle: "TxtLoadOptions"
second_title: "Riferimento API Aspose.Words per C++"
description: "Costruttore Aspose::Words::Loading::TxtLoadOptions::TxtLoadOptions. Inizializza una nuova istanza di questa classe con valori predefiniti in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.loading/txtloadoptions/txtloadoptions/
---
## TxtLoadOptions::TxtLoadOptions constructor


Inizializza una nuova istanza di questa classe con i valori predefiniti.

```cpp
Aspose::Words::Loading::TxtLoadOptions::TxtLoadOptions()
```


## Esempi



Mostra come leggere e visualizzare i collegamenti ipertestuali.
```cpp
const System::String inputText = System::String(u"Some links in TXT:\n") + u"https://www.aspose.com/\n" + u"https://docs.aspose.com/words/net/\n";

{
    System::SharedPtr<System::IO::Stream> stream = System::MakeObject<System::IO::MemoryStream>();
    System::ArrayPtr<uint8_t> buf = System::Text::Encoding::get_ASCII()->GetBytes(inputText);
    stream->Write(buf, 0, buf->get_Length());
    auto loadOptions = System::MakeObject<Aspose::Words::Loading::TxtLoadOptions>();
    loadOptions->set_DetectHyperlinks(true);

    // Carica il documento con collegamenti ipertestuali.
    auto doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);

    // Stampa il testo dei collegamenti ipertestuali.
    for (auto&& field : System::IterateOver(doc->get_Range()->get_Fields()))
    {
        std::cout << field->get_Result() << std::endl;
    }

    ASSERT_EQ(doc->get_Range()->get_Fields()->idx_get(0)->get_Result().Trim(), u"https://www.aspose.com/");
    ASSERT_EQ(doc->get_Range()->get_Fields()->idx_get(1)->get_Result().Trim(), u"https://docs.aspose.com/words/net/");
}
```

## Vedi anche

* Class [TxtLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
