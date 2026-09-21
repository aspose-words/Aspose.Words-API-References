---
title: "Aspose::Words::Loading::ChmLoadOptions::ChmLoadOptions‑konstruktor"
linktitle: "ChmLoadOptions"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Loading::ChmLoadOptions::ChmLoadOptions‑konstruktor. Initierar en ny instans av denna klass med standardvärden i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.loading/chmloadoptions/chmloadoptions/
---
## ChmLoadOptions::ChmLoadOptions constructor


Initierar en ny instans av den här klassen med standardvärden.

```cpp
Aspose::Words::Loading::ChmLoadOptions::ChmLoadOptions()
```


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
