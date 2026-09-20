---
title: "Конструктор Aspose::Words::Loading::TxtLoadOptions::TxtLoadOptions"
linktitle: "TxtLoadOptions"
second_title: "Справочник API Aspose.Words для C++"
description: "Конструктор Aspose::Words::Loading::TxtLoadOptions::TxtLoadOptions. Инициализирует новый экземпляр этого класса со значениями по умолчанию в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.loading/txtloadoptions/txtloadoptions/
---
## TxtLoadOptions::TxtLoadOptions constructor


Инициализирует новый экземпляр этого класса со значениями по умолчанию.

```cpp
Aspose::Words::Loading::TxtLoadOptions::TxtLoadOptions()
```


## Примеры



Показывает, как читать и отображать гиперссылки.
```cpp
const System::String inputText = System::String(u"Some links in TXT:\n") + u"https://www.aspose.com/\n" + u"https://docs.aspose.com/words/net/\n";

{
    System::SharedPtr<System::IO::Stream> stream = System::MakeObject<System::IO::MemoryStream>();
    System::ArrayPtr<uint8_t> buf = System::Text::Encoding::get_ASCII()->GetBytes(inputText);
    stream->Write(buf, 0, buf->get_Length());
    auto loadOptions = System::MakeObject<Aspose::Words::Loading::TxtLoadOptions>();
    loadOptions->set_DetectHyperlinks(true);

    // Загрузить документ с гиперссылками.
    auto doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);

    // Вывести текст гиперссылок.
    for (auto&& field : System::IterateOver(doc->get_Range()->get_Fields()))
    {
        std::cout << field->get_Result() << std::endl;
    }

    ASSERT_EQ(doc->get_Range()->get_Fields()->idx_get(0)->get_Result().Trim(), u"https://www.aspose.com/");
    ASSERT_EQ(doc->get_Range()->get_Fields()->idx_get(1)->get_Result().Trim(), u"https://docs.aspose.com/words/net/");
}
```

## См. также

* Class [TxtLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
