---
title: "Aspose::Words::Saving::DocSaveOptions::get_AlwaysCompressMetafiles metodo"
linktitle: "get_AlwaysCompressMetafiles"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::DocSaveOptions::get_AlwaysCompressMetafiles metodo. Quando è false, i metafili piccoli non vengono compressi per motivi di prestazioni. Il valore predefinito è true, tutti i metafili sono compressi indipendentemente dalla loro dimensione in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.saving/docsaveoptions/get_alwayscompressmetafiles/
---
## DocSaveOptions::get_AlwaysCompressMetafiles method


Quando **false**, i piccoli metafile non vengono compressi per motivi di prestazioni. Il valore predefinito è **true**, tutti i metafile vengono compressi indipendentemente dalla loro dimensione.

```cpp
bool Aspose::Words::Saving::DocSaveOptions::get_AlwaysCompressMetafiles() const
```


## Esempi



Mostra come modificare la compressione dei metafili in un documento durante il salvataggio.
```cpp
// Apri un documento che contiene una formula Microsoft Equation 3.0.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Microsoft equation object.docx");

// Quando salviamo un documento, i metafili più piccoli non vengono compressi per motivi di prestazioni.
// Possiamo impostare un flag in un oggetto SaveOptions per comprimere ogni metafile durante il salvataggio.
// Alcuni editor, come LibreOffice, non possono leggere i metafili non compressi.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::DocSaveOptions>();
saveOptions->set_AlwaysCompressMetafiles(compressAllMetafiles);

doc->Save(get_ArtifactsDir() + u"DocSaveOptions.AlwaysCompressMetafiles.docx", saveOptions);
```

## Vedi anche

* Class [DocSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
