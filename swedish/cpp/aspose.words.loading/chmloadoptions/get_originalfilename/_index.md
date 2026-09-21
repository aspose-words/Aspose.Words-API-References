---
title: "Aspose::Words::Loading::ChmLoadOptions::get_OriginalFileName metod"
linktitle: "get_OriginalFileName"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Loading::ChmLoadOptions::get_OriginalFileName metod. Namnet på CHM-filen. Standardvärdet är null i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words.loading/chmloadoptions/get_originalfilename/
---
## ChmLoadOptions::get_OriginalFileName method


Namnet på CHM-filen. Standardvärdet är **null**.

```cpp
System::String Aspose::Words::Loading::ChmLoadOptions::get_OriginalFileName() const
```

## Anmärkningar


CHM-dokument kan innehålla länkar som refererar till samma dokument med filnamn. Aspose.Words stödjer sådana länkar och använder normalt [OriginalFileName](../../../aspose.words/document/get_originalfilename/) för att kontrollera om filen som refereras av en länk är den fil som laddas. Om ett dokument laddas från en ström bör dess ursprungliga filnamn anges explicit via denna egenskap, eftersom det inte kan bestämmas automatiskt.

Om ett CHM-dokument laddas från en fil och ett icke‑null‑värde för denna egenskap anges, kommer värdet att ha företräde framför det faktiska filnamnet som lagras i [OriginalFileName](../../../aspose.words/document/get_originalfilename/).

## Exempel



Visar hur man löser URL:er som "ms-its:myfile.chm::/index.htm".
```cpp
// Vårt dokument innehåller URL:er som "ms-its:amhelp.chm::....htm", men det har ett annat namn,
// så fungerar inte fillänkarna efter att den sparats som HTML.
// Vi måste definiera det ursprungliga filnamnet i 'ChmLoadOptions' för att undvika detta beteende.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::ChmLoadOptions>();
loadOptions->set_OriginalFileName(u"amhelp.chm");

auto doc = System::MakeObject<Aspose::Words::Document>(System::MakeObject<System::IO::MemoryStream>(System::IO::File::ReadAllBytes(get_MyDir() + u"Document with ms-its links.chm")), loadOptions);

doc->Save(get_ArtifactsDir() + u"ExChmLoadOptions.OriginalFileName.html");
```

## Se även

* Class [ChmLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
