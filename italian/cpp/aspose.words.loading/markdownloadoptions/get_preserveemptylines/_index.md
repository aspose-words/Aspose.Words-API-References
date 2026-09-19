---
title: "Aspose::Words::Loading::MarkdownLoadOptions::get_PreserveEmptyLines metodo"
linktitle: "get_PreserveEmptyLines"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Loading::MarkdownLoadOptions::get_PreserveEmptyLines metodo. Ottiene o imposta un valore booleano che indica se preservare le righe vuote durante il caricamento di un documento Markdown. Il valore predefinito è false. Normalmente, le righe vuote tra gli elementi di blocco in Markdown sono ignorate. Le righe vuote all'inizio e alla fine del documento sono anch'esse ignorate. Questa opzione consente di importare tali righe vuote in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.loading/markdownloadoptions/get_preserveemptylines/
---
## MarkdownLoadOptions::get_PreserveEmptyLines method


Ottiene o imposta un valore booleano che indica se preservare le righe vuote durante il caricamento di un documento [Markdown](../../../aspose.words/loadformat/). Il valore predefinito è **false**. Normalmente, le righe vuote tra gli elementi di blocco in Markdown sono ignorate. Le righe vuote all'inizio e alla fine del documento sono anch'esse ignorate. Questa opzione consente di importare tali righe vuote.

```cpp
bool Aspose::Words::Loading::MarkdownLoadOptions::get_PreserveEmptyLines() const
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
