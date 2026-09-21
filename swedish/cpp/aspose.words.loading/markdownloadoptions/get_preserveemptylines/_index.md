---
title: "Aspose::Words::Loading::MarkdownLoadOptions::get_PreserveEmptyLines‑metod"
linktitle: "get_PreserveEmptyLines"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Loading::MarkdownLoadOptions::get_PreserveEmptyLines‑metod. Hämtar eller anger ett booleskt värde som indikerar om tomma rader ska bevaras när ett Markdown‑dokument laddas. Standardvärdet är false. Vanligtvis ignoreras tomma rader mellan blocknivåelement i Markdown. Tomma rader i början och slutet av dokumentet ignoreras också. Detta alternativ möjliggör import av sådana tomma rader i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words.loading/markdownloadoptions/get_preserveemptylines/
---
## MarkdownLoadOptions::get_PreserveEmptyLines method


Hämtar eller anger ett booleskt värde som indikerar om tomma rader ska bevaras när ett [Markdown](../../../aspose.words/loadformat/)‑dokument laddas. Standardvärdet är **false**. Vanligtvis ignoreras tomma rader mellan blocknivåelement i Markdown. Tomma rader i början och slutet av dokumentet ignoreras också. Detta alternativ möjliggör import av sådana tomma rader.

```cpp
bool Aspose::Words::Loading::MarkdownLoadOptions::get_PreserveEmptyLines() const
```


## Exempel



Visar hur man bevarar tomma rader när ett dokument laddas.
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

## Se även

* Class [MarkdownLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
