---
title: "Aspose::Words::Loading::TxtLoadOptions::get_DetectHyperlinks yöntemi"
linktitle: "get_DetectHyperlinks"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Loading::TxtLoadOptions::get_DetectHyperlinks yöntemi. Metinde hiperlinklerin algılanıp algılanmayacağını belirtir. Varsayılan değer C++'ta false'tur."
type: docs
weight: 3500
url: /tr/cpp/aspose.words.loading/txtloadoptions/get_detecthyperlinks/
---
## TxtLoadOptions::get_DetectHyperlinks method


Metinde hiperlinkleri algılayıp algılamayacağını belirtir. Varsayılan değer **false**.

```cpp
bool Aspose::Words::Loading::TxtLoadOptions::get_DetectHyperlinks() const
```


## Örnekler



Hipermetin bağlantılarını okuma ve gösterme yöntemini gösterir.
```cpp
const System::String inputText = System::String(u"Some links in TXT:\n") + u"https://www.aspose.com/\n" + u"https://docs.aspose.com/words/net/\n";

{
    System::SharedPtr<System::IO::Stream> stream = System::MakeObject<System::IO::MemoryStream>();
    System::ArrayPtr<uint8_t> buf = System::Text::Encoding::get_ASCII()->GetBytes(inputText);
    stream->Write(buf, 0, buf->get_Length());
    auto loadOptions = System::MakeObject<Aspose::Words::Loading::TxtLoadOptions>();
    loadOptions->set_DetectHyperlinks(true);

    // Hipermetin bağlantılı belgeyi yükle.
    auto doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);

    // Hipermetin bağlantı metnini yazdır.
    for (auto&& field : System::IterateOver(doc->get_Range()->get_Fields()))
    {
        std::cout << field->get_Result() << std::endl;
    }

    ASSERT_EQ(doc->get_Range()->get_Fields()->idx_get(0)->get_Result().Trim(), u"https://www.aspose.com/");
    ASSERT_EQ(doc->get_Range()->get_Fields()->idx_get(1)->get_Result().Trim(), u"https://docs.aspose.com/words/net/");
}
```

## Ayrıca Bakınız

* Class [TxtLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
