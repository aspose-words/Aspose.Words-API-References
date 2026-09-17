---
title: "Constructeur Aspose::Words::Loading::TxtLoadOptions::TxtLoadOptions"
linktitle: "TxtLoadOptions"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Constructeur Aspose::Words::Loading::TxtLoadOptions::TxtLoadOptions. Initialise une nouvelle instance de cette classe avec les valeurs par défaut en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.loading/txtloadoptions/txtloadoptions/
---
## TxtLoadOptions::TxtLoadOptions constructor


Initialise une nouvelle instance de cette classe avec les valeurs par défaut.

```cpp
Aspose::Words::Loading::TxtLoadOptions::TxtLoadOptions()
```


## Exemples



Montre comment lire et afficher les hyperliens.
```cpp
const System::String inputText = System::String(u"Some links in TXT:\n") + u"https://www.aspose.com/\n" + u"https://docs.aspose.com/words/net/\n";

{
    System::SharedPtr<System::IO::Stream> stream = System::MakeObject<System::IO::MemoryStream>();
    System::ArrayPtr<uint8_t> buf = System::Text::Encoding::get_ASCII()->GetBytes(inputText);
    stream->Write(buf, 0, buf->get_Length());
    auto loadOptions = System::MakeObject<Aspose::Words::Loading::TxtLoadOptions>();
    loadOptions->set_DetectHyperlinks(true);

    // Charger le document avec des hyperliens.
    auto doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);

    // Imprimer le texte des hyperliens.
    for (auto&& field : System::IterateOver(doc->get_Range()->get_Fields()))
    {
        std::cout << field->get_Result() << std::endl;
    }

    ASSERT_EQ(doc->get_Range()->get_Fields()->idx_get(0)->get_Result().Trim(), u"https://www.aspose.com/");
    ASSERT_EQ(doc->get_Range()->get_Fields()->idx_get(1)->get_Result().Trim(), u"https://docs.aspose.com/words/net/");
}
```

## Voir aussi

* Class [TxtLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
