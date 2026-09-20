---
title: "Aspose::Words::Loading::TxtLoadOptions::TxtLoadOptions constructor"
linktitle: "TxtLoadOptions"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Loading::TxtLoadOptions::TxtLoadOptions constructor. Inicializa una nueva instancia de esta clase con valores predeterminados en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.loading/txtloadoptions/txtloadoptions/
---
## TxtLoadOptions::TxtLoadOptions constructor


Inicializa una nueva instancia de esta clase con valores predeterminados.

```cpp
Aspose::Words::Loading::TxtLoadOptions::TxtLoadOptions()
```


## Ejemplos



Muestra cómo leer y mostrar hipervínculos.
```cpp
const System::String inputText = System::String(u"Some links in TXT:\n") + u"https://www.aspose.com/\n" + u"https://docs.aspose.com/words/net/\n";

{
    System::SharedPtr<System::IO::Stream> stream = System::MakeObject<System::IO::MemoryStream>();
    System::ArrayPtr<uint8_t> buf = System::Text::Encoding::get_ASCII()->GetBytes(inputText);
    stream->Write(buf, 0, buf->get_Length());
    auto loadOptions = System::MakeObject<Aspose::Words::Loading::TxtLoadOptions>();
    loadOptions->set_DetectHyperlinks(true);

    // Cargar documento con hipervínculos.
    auto doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);

    // Imprimir texto de los hipervínculos.
    for (auto&& field : System::IterateOver(doc->get_Range()->get_Fields()))
    {
        std::cout << field->get_Result() << std::endl;
    }

    ASSERT_EQ(doc->get_Range()->get_Fields()->idx_get(0)->get_Result().Trim(), u"https://www.aspose.com/");
    ASSERT_EQ(doc->get_Range()->get_Fields()->idx_get(1)->get_Result().Trim(), u"https://docs.aspose.com/words/net/");
}
```

## Ver también

* Class [TxtLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
