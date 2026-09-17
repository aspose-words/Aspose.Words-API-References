---
title: "Aspose::Words::Loading::TxtLoadOptions::get_DetectHyperlinks méthode"
linktitle: "get_DetectHyperlinks"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Loading::TxtLoadOptions::get_DetectHyperlinks méthode. Spécifie s'il faut détecter les hyperliens dans le texte. La valeur par défaut est false en C++."
type: docs
weight: 3500
url: /fr/cpp/aspose.words.loading/txtloadoptions/get_detecthyperlinks/
---
## TxtLoadOptions::get_DetectHyperlinks method


Spécifie s'il faut détecter les hyperliens dans le texte. La valeur par défaut est **false**.

```cpp
bool Aspose::Words::Loading::TxtLoadOptions::get_DetectHyperlinks() const
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
