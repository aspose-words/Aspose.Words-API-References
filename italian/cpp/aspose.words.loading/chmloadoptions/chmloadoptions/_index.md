---
title: "Aspose::Words::Loading::ChmLoadOptions::ChmLoadOptions costruttore"
linktitle: "ChmLoadOptions"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Loading::ChmLoadOptions::ChmLoadOptions costruttore. Inizializza una nuova istanza di questa classe con valori predefiniti in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.loading/chmloadoptions/chmloadoptions/
---
## ChmLoadOptions::ChmLoadOptions constructor


Inizializza una nuova istanza di questa classe con i valori predefiniti.

```cpp
Aspose::Words::Loading::ChmLoadOptions::ChmLoadOptions()
```


## Esempi



Mostra come risolvere URL come "ms-its:myfile.chm::/index.htm".
```cpp
// Il nostro documento contiene URL come "ms-its:amhelp.chm::....htm", ma ha un nome diverso,
// quindi i collegamenti ai file non funzionano dopo averlo salvato in HTML.
// È necessario definire il nome file originale in 'ChmLoadOptions' per evitare questo comportamento.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::ChmLoadOptions>();
loadOptions->set_OriginalFileName(u"amhelp.chm");

auto doc = System::MakeObject<Aspose::Words::Document>(System::MakeObject<System::IO::MemoryStream>(System::IO::File::ReadAllBytes(get_MyDir() + u"Document with ms-its links.chm")), loadOptions);

doc->Save(get_ArtifactsDir() + u"ExChmLoadOptions.OriginalFileName.html");
```

## Vedi anche

* Class [ChmLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
