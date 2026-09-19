---
title: "Aspose::Words::Loading::ChmLoadOptions::get_OriginalFileName metodo"
linktitle: "get_OriginalFileName"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Loading::ChmLoadOptions::get_OriginalFileName metodo. Il nome del file CHM. Il valore predefinito è null in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.loading/chmloadoptions/get_originalfilename/
---
## ChmLoadOptions::get_OriginalFileName method


Il nome del file CHM. Il valore predefinito è **null**.

```cpp
System::String Aspose::Words::Loading::ChmLoadOptions::get_OriginalFileName() const
```

## Note


I documenti CHM possono contenere collegamenti che fanno riferimento allo stesso documento per nome file. Aspose.Words supporta tali collegamenti e normalmente utilizza [OriginalFileName](../../../aspose.words/document/get_originalfilename/) per verificare se il file a cui si fa riferimento è il file che viene caricato. Se un documento viene caricato da uno stream, il suo nome file originale deve essere specificato esplicitamente tramite questa proprietà, poiché non può essere determinato automaticamente.

Se un documento CHM viene caricato da un file e viene specificato un valore non nullo per questa proprietà, il valore avrà la priorità sul nome reale del file memorizzato in [OriginalFileName](../../../aspose.words/document/get_originalfilename/).

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
