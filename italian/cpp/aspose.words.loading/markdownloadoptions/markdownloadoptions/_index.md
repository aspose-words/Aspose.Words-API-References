---
title: "Costruttore Aspose::Words::Loading::MarkdownLoadOptions::MarkdownLoadOptions"
linktitle: "MarkdownLoadOptions"
second_title: "Riferimento API Aspose.Words per C++"
description: "Costruttore Aspose::Words::Loading::MarkdownLoadOptions::MarkdownLoadOptions. Inizializza una nuova istanza della classe MarkdownLoadOptions in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.loading/markdownloadoptions/markdownloadoptions/
---
## MarkdownLoadOptions::MarkdownLoadOptions constructor


Inizializza una nuova istanza della classe [MarkdownLoadOptions](../).

```cpp
Aspose::Words::Loading::MarkdownLoadOptions::MarkdownLoadOptions()
```


## Esempi



Mostra come preservare le righe vuote durante il caricamento di un documento.
```cpp
System::String mdText = System::String::Format(u"{0}Line1{1}{2}Line2{3}{4}", System::Environment::get_NewLine(), System::Environment::get_NewLine(), System::Environment::get_NewLine(), System::Environment::get_NewLine(), System::Environment::get_NewLine());
{
    auto stream = System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_UTF8()->GetBytes(mdText));
    auto loadOptions = System::MakeObject<Aspose::Words::Loading::MarkdownLoadOptions>();
    loadOptions->set_PreserveEmptyLines(true);
    auto doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);

    ASSERT_EQ(u"\rLine1\r\rLine2\r\f", doc->GetText());
}
```

## Vedi anche

* Class [MarkdownLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
